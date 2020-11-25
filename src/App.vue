<template>

  <main>
    <div class="img-wrapper">
      <img alt="DAO logo" src="./assets/logo_dao.png" />
    </div>
    <Link />
    <SocialNetwork class="social"/>
  </main>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import SocialNetwork from './components/SocialNetwork.vue';
import Link from './components/Link.vue';

@Options({
  components: {
    SocialNetwork,
    Link
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">

* {
  margin: 0px;
  padding: 0px;
}

body {
  background-color: #3D3B3C
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
main {
  height: 100vh;
  max-width: 680px;
  margin-left: auto;
  margin-right: auto;
  padding-left: 20px;
  padding-right: 20px;
  display: flex;
  flex-direction: column;


  .social {
    margin-top: auto;
    margin-bottom: 60px;
  }
}

a {
  text-decoration: none;
  color: unset;
}

.img-wrapper {
  width: 100%;
  height: 200px;
}
img {
  width: 100%;
  height: 100%;
}


</style>
