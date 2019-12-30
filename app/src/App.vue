<template>
  <div id="app">
    <TestOne/>
    <TestTwo/>

  </div>
</template>

<script>

import TestTwo from './components/TestTwo.vue';
import TestOne from './components/TestOne.vue';

export default {
  name: 'app',
  components: {
    TestOne,
    TestTwo
  }
}
</script>

<style>


</style>
