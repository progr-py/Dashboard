<template >
  <div id="a">


    <div class="container">
      <aside-bar></aside-bar>
      <main-bar></main-bar>
      <rigth-bar></rigth-bar>

    </div>
  </div>
</template>

<script>

import aside from './components/aside.vue'
import main from './components/main.vue'
import rigth from './components/rigth.vue'
export default {
  components: {
    'aside-bar': aside,
    'main-bar': main,
    'rigth-bar': rigth
  },
  data() {
    return {

    };
  },
};

</script>
<style>

</style>
