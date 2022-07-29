<template>
  <div class="flex flex-col items-center">
    <h1>{{ title }}</h1>
    <Modal
      v-if="showModal"
      :header="header"
      :text="text"
      theme="sale"
      @close="toggleModal"
    />
    <button @click="toggleModal">Open Modal</button>
  </div>
</template>


<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  data() {
    return {
      title: "My First Vue App :)",
      header: "Sign up",
      text: "Grab your courses now!",
      showModal: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
  },
  components: {
    Modal,
  },
};
</script>
