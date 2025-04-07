<script>
export default {
  data() {
    return {
      todos: [
        {
          userId: 1,
          id: 1,
          title: "delectus aut autem",
          completed: false,
          imgCompleted: "/square-check-solid.svg",
          imgAlt: "Task Completed",
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
          imgCompleted: "/square-check-solid.svg",
          imgAlt: "Task Completed",
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
          imgCompleted: "/square-check-solid.svg",
          imgAlt: "Task Completed",
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
          imgCompleted: "/square-check-solid.svg",
          imgAlt: "Task Completed",
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
          imgCompleted: "/square-check-solid.svg",
          imgAlt: "Task Completed",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="hero">
    <h1>Seja bem vindo a diretivas Bind ou Vínculo</h1>
    <h2>Segue abaixo o código:</h2>
  </div>

  <section class="content-toDo">
    <p v-for="(obj, index) in todos">
      {{ index + 1 + " -" }}
      {{ obj.title[0].toUpperCase() + obj.title.slice(1).toLowerCase() }}
      <img
        v-if="obj.completed"
        class="img"
        v-bind:src="obj.imgCompleted"
        :alt="obj.imgAlt"
      />
      <img
        v-else=""
        class="img"
        v-bind:src="'/square.svg'"
        :alt="'Task Not Complete'"
      />
    </p>
  </section>
</template>

<style lang="scss" scoped>
h2 {
  margin-bottom: 1rem;
}

section.content-toDo {
  display: flex;
  flex-direction: column;
  row-gap: 0.5rem;

  p {
    display: flex;
    align-items: center;
    column-gap: 0.75rem;
    img {
      max-width: 1.5rem;
      max-height: 1.5rem;
    }
  }
}
</style>
