<template>
  <div class="home">
    <HomeComponent msg="Domain search is with you everywhere"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HomeComponent from '@/components/HomeComponent.vue'

export default {
  name: 'Home',
  components: {
    HomeComponent
  }
}
</script>
