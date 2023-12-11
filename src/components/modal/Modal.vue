<template>
  <div class="modal hidden" :id="idName">
    <div class="modal__content">

    </div>
  </div>
</template>

<script>
  export default {
    name:'modal',
    data(){
      return{
        idName:'modal'
      }
    },

  }
</script>

<style scoped>
  .modal{
    position: fixed;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(0,0,0,0.7);
    backdrop-filter: blur(10px);
  }
  .modal__content {
    position: relative;
    background-color: var(--color-primary);
    width: min(50%,502px);
    height: 243px;
    border-radius: 16px;
  }
  .hidden{
    visibility: hidden;
    opacity: 0;
  }
</style>