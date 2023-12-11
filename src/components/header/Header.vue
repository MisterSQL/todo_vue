<template>
  <header class="header">
    <div class="header__container container">
      <appLogo/>
      <buttonVue
          @customEvent="openModal"
          class="header__button"
          :label="label"/>
    </div>

  </header>
</template>

<script>
  import buttonVue from "@/components/ui/Button.vue";
  import appLogo from "@/components/header/AppLogo.vue";
  import modal from "@/components/modal/Modal.vue";

  export default {
    components:{
      buttonVue,
      appLogo,
      modal,
    },
    data() {
      return {
        label:"Создать",
      }
    },
    methods: {
      openModal() {
        const idName = modal.data().idName;
        const modalWindow = document.getElementById(idName);
        modalWindow.classList.remove('hidden');
      }
    }

  }
</script>

<style scoped>
  @import "@/assets/style/variables.css";
  @import "@/assets/style/global.css";


  .header__button {
    border: 1px solid white;
    color: var(--color-primary);
    border-radius: 2px;
    height: 36px;
    padding-inline: 26px;
    text-transform: uppercase;
    transition: .4s;
  }

  .header__button:hover {
    background-color: var(--color-primary);
    color: var(--color-secondary);
  }

  .header {
    background-color: var(--color-secondary);
    width: 100%;
  }

  .header__container {
    display: flex;
    align-items: center;
    margin: 0 auto;
    justify-content: space-between;
    padding-block: 16px;
  }

  @media screen and (max-width: 1435px) {
    .container {
      --container-padding: 128px;
    }
  }

  @media screen and (max-width: 1024px) {
    .container {
      --container-padding: 64px;
    }
  }

  @media screen and (max-width: 740px) {
    .container {
      --container-padding: 16px;
    }
  }
</style>