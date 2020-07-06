<template>
  <div class="domains">
    <h1>List of all domains searched by customers</h1>
    <p>
      In the links bellow you can find our two services! Go ahead and try them.
    </p>
    <b-container class="bv-row">
      <b-row>
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
