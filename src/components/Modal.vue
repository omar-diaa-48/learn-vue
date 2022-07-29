<template>
  <div
    @click.self="closeModal"
    class="top-0 fixed bg-slate-500 bg-opacity-50 w-full h-full"
  >
    <div class="w-96 p-5 mx-auto my-24 bg-white rounded-lg">
      <slot name="content" />
      <slot name="links" />
    </div>
  </div>
</template>

<script>
export default {
  props: ["header", "text"],
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>
