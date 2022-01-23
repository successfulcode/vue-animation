<template>
  <div>
    <InOutAnimation />
  </div> 
</template>

<script lang="ts">
import InOutAnimation from '@/components/InOutAnimation.vue';
import Vue from 'vue';

export default Vue.extend({
  components: { InOutAnimation },
  name: 'Enter_leave_animations',
});
</script>

<style>

</style>