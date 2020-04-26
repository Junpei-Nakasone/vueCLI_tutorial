<template>
<div>
<LikeHeader></LikeHeader>
<h2>{{ number }}</h2>
<LikeNumber v-bind:totalNumber="number" v-on:my-click="number = $event"></LikeNumber>
<p>{{ number }}</p>
<LikeNumber v-bind:totalNumber="number"></LikeNumber>
</div>
</template>

<script>
import LikeHeader from './components/LikeHeader.vue';

export default {
  data() {
    return {
      number: 10
    };
  },
  components: {
    LikeHeader
  }
}
</script>

<style scoped>
div {
  border: 1px solid blue;
}
</style>