<template>
  <div class="home-component">
    <h1>{{ msg }}</h1>
    <p>
      In the links bellow you can find our two services! Go ahead and try them.
    </p>
    <b-container class="bv-row">
      <b-row>
        <b-col>
          <b-card tag="article" style="max-width: 20rem;" class="mb-1">
            <img alt="Domain logo" style="width:60px" class="card-img-top" src="../assets/language-24px.svg">
            <b-card-body>
              <b-card-title>
                Find domains
              </b-card-title>
              <b-card-text>
                Our API will retrieve information about a specific domain.
              </b-card-text>

              <b-button to="/search" variant="outline-success">Specific domain!</b-button>
            </b-card-body>
          </b-card>
        </b-col>
        <b-col>
          <b-card tag="article" style="max-width: 20rem;" class="mb-2">
            <img alt="Domain logo" style="width:60px" class="card-img-top" src="../assets/history-24px.svg">
            <b-card-body>
              <b-card-title>
                List all domains
              </b-card-title>
              <b-card-text>
                This will give you all the domains that have been requested through our API.
              </b-card-text>

              <b-button to="/domains" variant="outline-primary">All domains!</b-button>
            </b-card-body>
          </b-card>
        </b-col>
      </b-row>
    </b-container>
    
  </div>
</template>

<script>
export default {
  name: 'HomeComponent',
  props: {
    msg: String
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
</style>
