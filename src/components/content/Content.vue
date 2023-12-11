<template>
  <div class="container main">
    <h1>{{innerTextTitle}}</h1>
    <listTodo/>
  </div>
</template>


<script>
  import listTodo from "@/components/content/List-task.vue";
  export default {
    name:'content_todo',
    data(){
      return{
        innerTextTitle:"Список задач"
      }
    },
    components:{
      listTodo
    }
  }

</script>

<style scoped>
  .main{
    margin-top: 53px;
  }

</style>

