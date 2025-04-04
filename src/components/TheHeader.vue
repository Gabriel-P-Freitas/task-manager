<script>
export default {
  data() {
    return {
      msg: `Seja bem vindo:`,
      showHeader: true,
      acessLevel: "Marketing",
    };
  },
};
</script>

<template>
  <header v-show="showHeader" class="header">
    <h1 v-if="acessLevel === 'Admin'">
      {{ msg }} <span>{{ acessLevel }}</span>
    </h1>
    <h1 v-if="acessLevel === 'Marketing'">
      {{ msg }} <span>{{ acessLevel }}</span>
    </h1>
    <h1 v-if="acessLevel === 'User'">
      {{ msg }} <span>{{ acessLevel }}</span>
    </h1>

    <nav>
      <ul>
        <li>Item 1</li>
        <li>Item 2</li>
        <li>Item 3</li>
        <li>Item 4</li>
      </ul>
    </nav>
  </header>
</template>

<style>
.header {
  display: flex;
  justify-content: space-between;
  width: 90ch;
  margin: 0 auto;
}
.header h1 {
  color: white;
}

.header nav ul {
  display: flex;
  gap: 1.5rem;
}

.header nav ul li {
}
</style>
