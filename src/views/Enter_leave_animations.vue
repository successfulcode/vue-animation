<template>
  <div>
    <div>
      <InOutAnimationIf />
    </div> 

    If else
    <div>
      <InOutIfElse />
    </div>
</div>

</template>

<script lang="ts">
import InOutAnimationIf from '@/components/InOutAnimationIf.vue';
import InOutIfElse from '@/components/InOutIfElse.vue';
import Vue from 'vue';

export default Vue.extend({
  components: { InOutAnimationIf, InOutIfElse },
  name: 'Enter_leave_animations',
});
</script>

<style>

</style>