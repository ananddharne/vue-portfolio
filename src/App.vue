<template>
    <v-app light = true>
    <v-toolbar app>
      <div class="text-xs-center">
       <router-link to="/home">
      <v-btn small color="grey darken-1">
   <v-icon dark>home</v-icon>Home
 </v-btn>
 </router-link>
 <router-link to="/CV">
 <v-btn small color="grey darken-1">
   <v-icon dark>school</v-icon>CV
</v-btn>
</router-link>
<router-link to="/Forum">
<v-btn small color="grey darken-1">Forum
<v-icon dark>forum</v-icon>
</v-btn>
</router-link>
<v-btn small color="grey darken-1">
<v-icon dark>face</v-icon>Portfolio
</v-btn>
</div>
    </v-toolbar>
    <v-content>
        <v-container fluid> <router-view> </router-view></v-container>
      </v-content>
  <vue-progress-bar></vue-progress-bar>
  </v-app>
</template>

<script>
export default {
  mounted () {
    //  [App.vue specific] When App.vue is finish loading finish the progress bar
    this.$Progress.finish()
  },
  created () {
    //  [App.vue specific] When App.vue is first loaded start the progress bar
    this.$Progress.start()
    //  hook the progress bar to start before we move router-view
    this.$router.beforeEach((to, from, next) => {
      //  does the page we want to go to have a meta.progress object
      if (to.meta.progress !== undefined) {
        let meta = to.meta.progress
        // parse meta tags
        this.$Progress.parseMeta(meta)
      }
      //  start the progress bar
      this.$Progress.start()
      //  continue to next page
      this.$Progress.increase(30)
      this.$Progress.increase(50)
      this.$Progress.increase(100)


      next()
    })
    //  hook the progress bar to finish after we've finished moving router-view
    this.$router.afterEach((to, from) => {
      //  finish the progress bar
      // this.$Progress.finish()
    })
  }
}
</script>

<style>
.text-xs-center {

  margin: auto;
  width: 90%;

}
</style>
