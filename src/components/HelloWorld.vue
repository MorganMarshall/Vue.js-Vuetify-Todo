<template>
  <div class="hello">
    <v-toolbar>

      <v-toolbar-title>Vue Material</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">

        <v-btn flat>Vue.js</v-btn>
        <v-btn flat>Vuetify</v-btn>
        <v-btn flat>Github</v-btn>
      </v-toolbar-items>
    </v-toolbar>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
