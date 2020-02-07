<template>
  <q-page padding>
    <input
      v-model="message"
      @keyup.esc="clearMessage"
      @keyup.enter="alertMessage"
      v-autofocus
      :style="errorStyle"
    />
    <button @click="clearMessage">Clear</button>
    <h5 class="border-grey" v-show="message.length">{{message}}</h5>
    <h5 v-if="message.length">Test if</h5>
    <h6 v-else>Test else</h6>
    <div>{{message.length}}</div>

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
    },
    errorStyle() {
      if (this.message.length > 22) {
        return {
          color: "red",
          background: "pink"
        };
      }
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
  },
  directives: {
    autofocus: {
      inserted(el) {
        el.focus();
      }
    }
  },
  beforeCreate() {
    console.log("beforeCreate");
  },
  created() {
    console.log("created");
  },
  beforeMount() {
    console.log("beforeMount");
  },
  mounted() {
    console.log("mounted");
  },
  beforeUpdate() {
    console.log("beforeUpdate");
  },
  updated() {
    console.log("updated");
  },
  beforeDestroy() {
    console.log("beforeDestroy");
  },
  destroyed() {
    console.log("destroyed");
  }
};
</script>
 
<style>
.border-grey {
  border: 1px solid grey;
}
.error {
  color: red;
  background: pink;
}
</style>