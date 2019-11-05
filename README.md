# huff_n_puff
Huff'n'Puff Team Project, INF 554 Information Visualization, Fall 2019, USC


A possible alternative for Huff'n'Puff has been implemented at:
http://pdms.usc.edu/~pvhumphr/huff_n_puff/project_01/dist/

The repository is at:
https://github.com/phumphri/huff_n_puff.git

The technology stack is comprised of Vue.js and d3.js.

There will be a Vue.component for each row in the website.
Within each row Vue.component, there will be one or more Vue.components for the graphics.
This will simplify development.

The typical procedure for adding a row with a graphic to the webpage:

1.  Copy and modify SampleBarChart.vue as <your topic graphic>.vue

2.  Copy and modify SampleRow.vue as <your topic row>.vue.

3.  Modify <your topic row>.vue to reference <your topic grapic>.vue

4.  Modify App.vue and add <your topic row>.vue to the template, script, and components.

This will allow you to focus on the story and your visualization and not worry about deployment.

The jumbotron from the lab exercises will be used as the first row of the webpage.

The sample Vue.components were based on the HelloWorld.vue in the lab exercies.
