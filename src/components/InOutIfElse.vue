<template>
  <div>
    <button @click="show=!show">IF ELSE IN</button>
     <transition name="slide-fade2">
      <div v-if="show" key="show">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste, ratione.
      </div>
      <div v-else>
        Else
      </div>
    </transition>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'InOutIfElse',
  data() {
    return {
      show: false,
    };
  },
});
</script>

<style lang="scss" scoped>
.slide-fade2-enter-active {
  transition: all .5s ease;
}
.slide-fade2-enter, .slide-fade2-leave-to {
  transform: translateX(100%);
}
</style>
