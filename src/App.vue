<template>
  <div id="portal-target"></div>
  <div id="app">
    <portal target="#portal-target">
      <Popup ref="popup" :title="'Popup test2'" :sub="'Erik Hanchett '">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda dolor
        saepe perspiciatis, facere rem iste doloribus ut illo fugit nam delectus
        aliquid totam voluptates neque deleniti sequi animi impedit adipisci.
      </Popup>
    </portal>
    <button class="btn" @click="$refs.popup.show = !$refs.popup.show">
      Open Modal
    </button>
  </div>
</template>

<script>
import Popup from "./components/Popup.vue";

export default {
  name: "App",
  data() {
    return {
      show: false
    };
  },
  components: {
    Popup
  }
};
</script>

<style lang="scss">
/* Demo Styles */

html,
body {
  height: 100%;
}

body {
  font: 600 18px/1.5 -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen-Sans, Ubuntu, Cantarell, "Helvetica Neue", sans-serif;
  background-image: linear-gradient(to right, #7f53ac 0, #657ced 100%);
  color: black;
}

a {
  color: inherit;
}

.container {
  display: grid;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

small {
  color: #aaa;
}

.btn {
  font-size: 36px;
  background-color: #fff;
  padding: 1em 1.5em;
  border-radius: 3px;
  text-decoration: none;
  i {
    padding-right: 0.3em;
  }
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
