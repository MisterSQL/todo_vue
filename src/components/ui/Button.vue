<template>
  <button
      @click="handleClick"
      class="button"
      type="button"
  >
    {{label}}
  </button>
</template>

<script>
  export default {
    name:'button_vue',
    props:{
      label:{
         type:String,
         required:false,
       },
    },
    methods:{
      handleClick(){
        this.$emit('customEvent');
      }
    },
  }
</script>


<style scoped>
  @import "@/assets/style/global.css";
  .button {
    background-color: transparent;
    color: var(--color-secondary);
    font-weight: 500;
  }

</style>