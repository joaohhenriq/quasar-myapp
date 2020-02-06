<template>
  <q-page padding>
    <input v-model="message" @keyup.esc="clearMessage" @keyup.enter="alertMessage" />
    <button @click="clearMessage">Clear</button>
    <h5 class="border-grey" v-show="message.length">{{message}}</h5>
    <h5 v-if="message.length">Test if</h5>
    <h6 v-else>Test else</h6>

    <hr />
    <p>Uppercase: {{messageUppercase}}</p>
    <P>Lowercase: {{message | messageLowercase}}</P>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      message: "Helloooooooo o o "
    };
  },
  computed: {
    messageUppercase() {
      return this.message.toUpperCase();
    }
  },
  methods: {
    clearMessage() {
      this.message = "";
    },
    alertMessage() {
      alert("asasasas");
    }
  },
  filters: {
    messageLowercase(value) {
      return value.toLowerCase();
    }
  }
};
</script>
 
<style>
.border-grey {
  border: 1px solid grey;
}
</style>