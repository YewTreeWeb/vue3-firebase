<template>
  <h2>{{ title }}</h2>
  <input type="text" ref="name" />
  <button @click="handleClick">Click Me</button>
</template>

<script>
export default {
  name: "VueThree",
  data() {
    return {
      title: "My First Component with Vue 3",
    };
  },
  methods: {
    handleClick() {
      // $refs give references to DOM elements
      console.log(this.$refs.name);
      this.$refs.name.classList.add("active");
      this.$refs.name.focus();
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
h2 {
  margin: 40px 0 0;
}
</style>
