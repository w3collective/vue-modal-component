<template>
  <div id="app">
    <button @click="openModal">Open</button>
    <DemoModal v-show="isModalVisible" @close="closeModal" />
  </div>
</template>

<script>
  import DemoModal from './components/DemoModal.vue';
  export default {
    name: 'App',
    components: {
      DemoModal,
    },
    data() {
      return {
        isModalVisible: false,
      };
    },
    methods: {
      openModal() {
        this.isModalVisible = true;
      },
      closeModal() {
        this.isModalVisible = false;
      }
    }
  };
</script>