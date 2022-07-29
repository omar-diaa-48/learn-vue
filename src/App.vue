<template>
  <div class="mt-8 flex flex-col items-center">
    <h1>{{ title }}</h1>
    <input class="border rounded" type="text" ref="name" />
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      title: "My First Vue App :)",
    };
  },
  methods: {
    handleClick() {
      this.$refs.name.focus();
    },
  },
};
</script>
