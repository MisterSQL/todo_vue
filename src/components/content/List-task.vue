<template>
  <div class="main__taskList">
    <task/>

  </div>
</template>

<script>
  import task from "@/components/content/Task.vue";
  export default {
    components:{
      task
    },

  }
</script>
<style scoped>
  .main__taskList {
    display: grid;
    --cards : 3;
    grid-template-columns: repeat(var(--cards),minmax(300px,600px));
    margin-top: 53px;
    gap: 50px;
  }

  @media screen and (max-width: 1184px) {
    .main__taskList{
      --cards: 2;
    }
  }

  @media screen and (max-width: 740px) {
    .main__taskList{
      --cards: 1;
    }
  }

</style>