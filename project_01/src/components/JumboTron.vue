<template>

    <div class="hello">
        <h1>{{ msg }}</h1>

        <!-- Bootstrap CSS -->
        <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
        <link rel="stylesheet" type="text/css" href="./public/jumbotron.css" />


        <nav class="navbar navbar-expand-md navbar-dark fixed-top bg-dark">
            <a class="navbar-brand" href="#">Navbar</a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExampleDefault" aria-controls="navbarsExampleDefault" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>

            <div class="collapse navbar-collapse" id="navbarsExampleDefault">
                <ul class="navbar-nav mr-auto">
                    <li class="nav-item active">
                        <a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Link</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link disabled" href="#">Disabled</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="dropdown01" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Dropdown</a>
                        <div class="dropdown-menu" aria-labelledby="dropdown01">
                            <a class="dropdown-item" href="#">Action</a>
                            <a class="dropdown-item" href="#">Another action</a>
                            <a class="dropdown-item" href="#">Something else here</a>
                        </div>
                    </li>
                </ul>
                <form class="form-inline my-2 my-lg-0">
                    <input class="form-control mr-sm-2" type="text" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
                </form>
            </div>
        </nav>

        <main role="main">

            <!-- Main jumbotron for a primary marketing message or call to action -->
            <div class="jumbotron">
                <div class="container">
                    <h1 class="display-3">700,000+ Trips</h1>
                    <p>This website examins trips, routes, and passholder behavior.</p>
                    <p><a class="btn btn-primary btn-lg" href="#" role="button">Learn more &raquo;</a></p>
                </div>
            </div>


            <div class="container">

                <!-- This row contains headings above the small Vue-components. -->
                <div class="row">
                    <div class="col-sm-4">
                        <h2>Trips</h2>
                    </div>
                    <div class="col-sm-4">
                        <h2>Routes</h2>
                    </div>
                    <div class="col-sm-4">
                        <h2>Passholders</h2>
                    </div>
                </div>

                <div class="row">
                    <div class="col-sm-4" id="small_trips_div_parent_1">
                        <SampleBarChart div_id="small_trips_div_1" parent_id="small_trips_div_parent_1" />
                    </div>
                    <div class="col-sm-4" id="small_trips_div_parent_2">
                        <SampleBarChart div_id="small_trips_div_2" parent_id="small_trips_div_parent_2" />
                    </div>
                    <div class="col-sm-4" id="small_trips_div_parent_3">
                        <SampleBarChart div_id="small_trips_div_3" parent_id="small_trips_div_parent_3" />
                    </div>
                </div>

                <div class="row">
                    <div class="col-sm-4">
                        <p>The amount, frequency, and seasonality of trips are examined.</p>
                        <p>This seeks to deteremine the number of bikes needed for various scenarios.</p>
                        <p><a class="btn btn-secondary" href="#" role="button">View details &raquo;</a></p>
                    </div>
                    <div class="col-sm-4">
                        <p>Start and corresponding stop stations are examined.</p>
                        <p>This seeks to deteremine where additional stations are needed or there is an excess of stations.</p>
                        <p><a class="btn btn-secondary" href="#" role="button">View details &raquo;</a></p>
                    </div>
                    <div class="col-sm-4">
                        <p>This seeks to determine who is using this service.</p>
                        <p><a class="btn btn-secondary" href="#" role="button">View details &raquo;</a></p>
                    </div>
                </div>
                <hr>

            </div>

        </main>

        <!-- <footer class="container">
            <p>&copy; Company 2017-{{ site.time | date: "%Y" }}</p>
        </footer> -->

    </div>


</template>


<script>

    window.onresize = function () { location.reload() }

    import SampleBarChart from './SampleBarChart.vue'

    export default {
        name: 'JumboTron',
        components: {
            SampleBarChart
        },
        props: {
            msg: String
        },
        mounted() {
            () => { }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: white;
    }
</style>