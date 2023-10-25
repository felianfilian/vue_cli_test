<template>
  <div>
    <ul>
      <li
        v-for="user in users"
        :key="user.name"
        @click="user.showAge = true"
        @keydown.enter="user.showAge = true"
        tabindex="0"
      >
        <p>{{ user.name }}</p>
        <p v-if="user.showAge">{{ user.age }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { name: 'Mario', age: 35, showAge: false },
        { name: 'Peach', age: 21, showAge: false },
      ],
    };
  },
};
</script>

<style lang="scss">
div ul {
  margin-top: 120px;
}
li {
  list-style: none;
  font-size: 20px;
}
</style>
