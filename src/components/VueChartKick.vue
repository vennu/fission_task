<template>
  <section class="container">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/chartjs">vue-chartjs</router-link></li>
      <li><router-link to="/chartkick">vue-chartkick</router-link></li>
    </ul>
    <h1>Demo examples of vue-chartkick</h1>

<xls-csv-parser :columns="columns" @onValidate="onValidate"  lang="en"></xls-csv-parser>
    <br><br>
   <div class="results" v-if="results">
      <h3>Results:</h3>
      <pre>{{ results }}</pre>
    </div>
    

    <div class="columns">
      <div class="column">
        <h3>Line Chart</h3>
        <line-chart :data="chartData" :download="true"></line-chart>
      </div>
     
     
    </div>
  </section>
</template>

<script>
  import { XlsCsvParser } from 'vue-xls-csv-parser'
  export default {
    name: 'VueChartKick',
    components: {
      XlsCsvParser
    },
    methods: {
      onValidate (results) {
        this.results = results
        console.log(this.results)
      }
    },
    data () {
      return {
        columns: [
          { name: 'Column 1', value: 'x-axis' },
          { name: 'Column 2', value: 'y-axis' }
        ],
        chartData: this.results,
        results: null
      }
    }
  }
</script>

<style scoped>
  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
