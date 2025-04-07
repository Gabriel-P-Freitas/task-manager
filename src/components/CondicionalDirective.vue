<script>
export default {
  data() {
    return {
      msg: `Seja bem vindo:`,
      name: "Fernando",
      showHeader: true,
      acessLevel: "Marketing",
    };
  },
};
</script>

<template>
  <header v-show="showHeader" class="header">
    <h1 v-if="acessLevel === 'Admin'">
      {{ msg }} <span class="span-name">{{ acessLevel }} {{ name }}</span>
    </h1>
    <h1 v-else-if="acessLevel === 'Marketing'">
      {{ msg }} <span class="span-name">{{ acessLevel }} {{ name }}</span>
    </h1>
    <h1 v-else="">
      {{ msg }} <span class="span-name">{{ acessLevel }} {{ name }}</span>
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

.header .span-name {
  background-color: rgba(255, 255, 6, 0.626);
}

.header nav ul {
  display: flex;
  gap: 1.5rem;
}

.header nav ul li {
}
</style>
