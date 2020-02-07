<template>
  <q-page padding>
    <ul>
      <li v-for="task in tasks">{{task}}</li>
    </ul>
    <hr />
    <ul>
      <li v-for="test in tests" :key="test.name">{{test.name}}, {{test.dueDate}}, {{test.dueTime}}</li>
    </ul>
    <hr />
    <task v-for="test in tests" :key="test.name" :prop="test">{{test.name}}</task>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      tasks: ["AAAAA", "BBBBB", "CCCCC"],
      tests: [
        {
          name: "gogogog",
          dueDate: "01/01/1001",
          dueTime: "15:15"
        },
        {
          name: "gegegege",
          dueDate: "01/01/1001",
          dueTime: "15:15"
        },
        {
          name: "kakakaka",
          dueDate: "01/01/1001",
          dueTime: "15:15"
        }
      ]
    };
  },
  components: {
    task: require("../components/Task.vue").default
  }
};
</script>

<style>
</style>