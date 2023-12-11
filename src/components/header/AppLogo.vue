<template>
  <div class="icon">
    TO<span :class="textColor">DO</span>S
  </div>
</template>
<script>


export default {
  name:'logo',
  data() {
    return {
      textColor: 'text-color-error',
    }
  },
}
</script>


<style scoped>
.icon {
  color: var(--color-primary);
}
.text-color-error {
  color: var(--error);
}
</style>