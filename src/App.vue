<template>
  <div id="app" @click="closeModal">
    <modal/>
    <header_todo/>
    <content_todo/>
  </div>
</template>

<script>

import header_todo from '@/components/header/Header.vue'
import content_todo from "@/components/content/Content.vue";
import modal from "@/components/modal/Modal.vue";

export default {
  name: 'app',
  components: {
    header_todo,
    content_todo,
    modal,
  },

  methods:{
    closeModal(event){
      const idModal = document.getElementById(modal.data().idName);
      const element = event.target;
      if(element.classList.contains('modal')) {
        idModal.classList.add('hidden');
      }
    }
  }
}
</script>

