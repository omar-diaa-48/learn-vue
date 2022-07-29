<template>
  <div class="flex flex-col items-center">
    <h1>{{ title }}</h1>
    <teleport to="#modal" v-if="showModal">
      <Modal :header="header" :text="text" @close="toggleModal">
        <template v-slot:content>
          <h1>Sign up</h1>
          <p>Grab your courses now!</p>
        </template>
        <template v-slot:links>
          <div class="flex justify-end">
            <button>Sign up</button>
            <button class="ml-2" @click="toggleModal">Cancel</button>
          </div>
        </template>
      </Modal>
    </teleport>
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
