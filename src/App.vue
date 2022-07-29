<template>
  <div class="flex flex-col items-center">
    <h1>{{ title }}</h1>
    <Modal v-if="showModal" :header="header" :text="text" @close="toggleModal">
      <template v-slot:content>
        <h1>{{ header }}</h1>
        <p>{{ text }}</p>
      </template>
      <template v-slot:links>
        <div class="flex justify-end">
          <button>Sign up</button>
          <button class="ml-2" @click="toggleModal">Cancel</button>
        </div>
      </template>
    </Modal>
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
