<template>
  <div class="domains">
    <h1>List of all domains searched by customers</h1>
    <p>
      In the next card you will find all the domains! Thank you for using our service.
    </p>
    <b-container class="bv-row">
      <b-row>
        <b-col>
          <b-card tag="article" class="mb-2">
            <img alt="Domain logo" style="width:60px" class="card-img-top" src="../assets/history-24px.svg">
            <b-card-body>
              <b-card-title>
                List all domains
              </b-card-title>
              <b-card-text>
                This will give you all the domains that have been requested through our API.
              </b-card-text>

              <ul class="list-group row" v-if="domains && domains.length">
                <li class="list-group-item col-xs-6 col-sm-4 col-md-3" v-for="domain of domains" v-bind:key="domain.id">
                  <p>{{domain.domain}}</p>
                </li>
              </ul>
              <br>
              <b-button to="/domains" onClick="window.location.reload();" variant="outline-primary">Refresh list</b-button>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      domains: [],
      errors_d: []
    }
  },

  // Fetches posts when the component is created.
  created() {

    axios.get(`http://localhost:3000/domains`)
    .then(response => {
      this.domains = response.data.items
      console.log(this.domains)
    })
    .catch(e_d => {
      this.errors_d.push(e_d)
    })

    // async / await version (created() becomes async created())
    //
    // try {
    //   const response = await axios.get(`http://jsonplaceholder.typicode.com/posts`)
    //   this.posts = response.data
    // } catch (e) {
    //   this.errors.push(e)
    // }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  padding: 10px;
  margin-top: 20px;
}
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
.card {
  margin: 0 auto;
}
.list-group {
  flex-direction: row;
  justify-content: center;
}
.list-group-item {
  border-top-width: 1px !important;
  margin-bottom: 2px;
}
</style>
