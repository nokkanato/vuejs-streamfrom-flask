<template>
  <v-content class="hello">
      <h1 style="padding-top:5%;"> OPL- videoStreming</h1>
    <v-layout row wrap>
        <v-flex xs12 md6>
          <div style="padding-top:10%;">
            <iframe :src="video" height="500px" width="100%;" frameborder="0"></iframe>
          </div>
        </v-flex>
        <v-flex xs12 md6>
              <div style="padding-top:10%;">
                <iframe :src="chat" height="500px" width="100%;" frameborder="0"></iframe>
              </div>
       </v-flex>
      </v-layout>
  </v-content>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      video: `http://${location.hostname}:4000/`,
      chat: `http://${location.hostname}:5000/`
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
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
