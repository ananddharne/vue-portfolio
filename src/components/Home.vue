<template>
  <v-app light = "true">
    <v-container>
      <v-layout justify-space around>
            <v-layout align-baseline row spacer slot="header">
               <v-flex xs12 sm6 md3>
                <v-avatar size="136px" slot="activator">
                  <img src="https://avatars0.githubusercontent.com/ananddharne" alt="">
                </v-avatar>
              </v-flex>
              <v-flex>
                <h1>Anand Dharne</h1>
                <span class="grey--text">Software developer(Web dev, Automated Testing and Dev-Ops)</span><br>
              </v-flex>
            </v-layout>
      </v-layout>
      <v-layout>

      <v-flex x12 m3 offset-xs3>
        <v-card color = "grey lighten-4">
              <v-layout fill-height>
                <v-flex xs12 align-end flexbox>
                </v-flex>
              </v-layout>
            <div>
              <span>Hello from Boston! I am a Software developer working currently for a start-up named <a href = "http://www.gethappie.me/home" target="_blank"> Happie </a></span><br><br>
              <span> I am proficient with javascript and their frameworks. Have done a fair amount of web development (Using <a href = "https://vuejs.org/" target="_blank">Vue.js</a> with <a href = "https://webpack.github.io" target="_blank"> Webpack </a> now)</span><br><br>
              <span> Amateur but enriching experience with ORM frameworks like Django. Used Python to build models. Also Implemented unit and API testing using the Nose framework in Python (Test Driven Development)  </span> <br> <br>
              <span>My current experience involves me working in different parts of the SDLC like setting up the test environment for the web application build (hooked up unit and e2e tests using a wide variety of frameworks predominantly <a href = "https://karma-runner.github.io/1.0/index.html" target="_blank">Karma </a>and<a href = "http://nightwatchjs.org/" target="_blank"> Nightwatch.js</a></span><br><br>
              <span> I am also fortunate enough to work with the build system since its early stages of the application being built. Sets up a new build system as  Dev-ops professional on <a href = "https://gitlab.com/" target="_blank">Gitlab CI</a>(moved to gitlab from <a href ="https://circleci.com/">circleCI</a>)</span><br><br>
              <span> Expereince with <a href = "https://www.docker.com/" target="_blank"> Docker</a> for build images for deployment on CI servers</span><br><br>

            </div>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
  <v-footer light="true" app>
    <v-layout row wrap align-center>
    <icon>
        <icon name="fa-github"></icon>
        <icon name="fa-linkedin"></icon>
        <icon name="fa-facebook"></icon>
      </icon>
        <v-icon class="red--text">favorite</v-icon>
        </div>
      </v-flex>
    </v-layout>
  </v-footer>
    </v-app>
</template>

<script>
import Icon from 'vue-awesome/components/Icon'

export default {
  name: 'Home',
  data () {
    return {
      msg: ''
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.centeravatar{
  width: 100%;
}
.fa-icon{

  width: 100%;
  height: 100%;
}
</style>
