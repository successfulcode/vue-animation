<template>
  <div>
    <button @click="show=!show">SHOW</button>
    <transition name="fade">
      <div v-if="show">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste, ratione.
      </div>
    </transition>

    <button @click="show1=!show1">SHOW1</button>
     <transition name="slide-fade">
      <div v-if="show1">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste, ratione.
      </div>
    </transition>

    <button @click="show2=!show2">SHOW2</button>
     <transition name="slide-fade2">
      <div v-if="show2">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Iste, ratione.
      </div>
    </transition>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'InOutAnimation',
  data() {
    return {
      show: false,
      show1: false,
      show2: false,
    };
  },
});
</script>

<style lang="scss" scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}


.slide-fade2-enter-active {
  transition: all .5s ease;
}
.slide-fade2-leave-active {
  transition: all .5s ease;
}
.slide-fade2-enter, .slide-fade2-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(100%);
  // opacity: 0;
}
</style>
