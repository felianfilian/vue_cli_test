<template>
  <div>
    <h4>{{ name }}</h4>
    <p>{{ sayHi() }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'mario',
    };
  },
  methods: {
    sayHi() {
      return `Hi ${this.name}`;
    },
  },
};
</script>

<style lang="scss"></style>
