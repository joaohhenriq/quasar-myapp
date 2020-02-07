<template>
  <q-page padding>
    <ul>
      <li v-for="task in tasks" :key="task">{{task}}</li>
    </ul>
    <hr />
    <ul>
      <li v-for="test in tests" :key="test">{{test.name}}, {{test.dueDate}}, {{test.dueTime}}</li>
    </ul>
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
  }
};
</script>

<style>
</style>