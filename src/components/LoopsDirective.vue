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
        },
        {
          userId: 1,
          id: 2,
          title: "quis ut nam facilis et officia qui",
          completed: false,
        },
        {
          userId: 1,
          id: 3,
          title: "fugiat veniam minus",
          completed: false,
        },
        {
          userId: 1,
          id: 4,
          title: "et porro tempora",
          completed: true,
        },
        {
          userId: 1,
          id: 5,
          title:
            "laboriosam mollitia et enim quasi adipisci quia provident illum",
          completed: false,
        },
      ],
    };
  },
};
</script>

<template>
  <div>
    <h1>Seja bem vindo as diretivas em Loops</h1>
    <h2>Lista de toDos percorridas abaixo:</h2>
  </div>

  <section class="content-toDo">
    <div class="" v-for="(obj, index) in todos" v-bind:key="obj.id">
      <p>
        {{ index + 1 }}. {{ obj.title }}
        <button class="btn-completed btn" v-if="obj.completed === true">
          Concluído
        </button>
        <button class="btn-incompleted btn" v-else="obj.completed === false">
          A fazer
        </button>
      </p>
    </div>
  </section>
</template>

<style lang="scss" scoped>
h2 {
  margin-bottom: 24px;
}

.content-toDo {
  display: flex;
  flex-direction: column;
  row-gap: 12px;
}

.btn {
  padding: 4px 8px;
  border-radius: 4px;
  border: 1px solid white;
  font-weight: bold;
  font-size: 12px;
  color: white;
  cursor: pointer;
}

.btn-completed {
  background-color: rgba(0, 243, 0, 0.329);
}

.btn-incompleted {
  background-color: rgba(243, 186, 0, 0.329);
}
</style>
