<template>
    <div>
        <div  v-bind:id="row_id" class="row ml-5">
            <div class="col-sm-12">
                <h1>Sample Row Title for {{row_id}}</h1>
            </div>
        </div>
        <div class="row">
            <div class="col-sm-2">
                <fileset class="mt-5">
                    <legend>Selection</legend>
                    <p><b>Placeholder for selection elements.</b></p>
                </fileset>
            </div>
            <div class="col-sm-2">
                <fileset class="mt-5">
                    <legend>Sort</legend>
                    <p><b>Placeholder for sorting options.</b></p>
                </fileset>
            </div>
            <div v-bind:id="col_id" class="col-sm-8">
                <fileset class="mt-5">
                    <legend>Graphic</legend>
                    <SampleBarChart v-bind:id="div_id" v-bind:parent_id="col_id" />
                </fileset>
            </div>
        </div>
    </div>

</template>

<script>
    // import * as d3 from "d3";
    // import VueLogger from 'vuejs-logger'
    import SampleBarChart from './SampleBarChart.vue'


    export default {
        name: "SampleRow",
        props: ["row_id", "col_id", "div_id"],
        components: {
            SampleBarChart
        },
        mounted() {
            () => { };
        }
    }
</script>