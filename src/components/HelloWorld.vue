<template>
  <div>
    <form action="" @submit.prevent="clickit">
      <input type="text" placeholder="email" v-model="email" />
      <input type="text" placeholder="password" v-model="password" />
      <button>Login</button>
    </form>
  </div>
</template>

<script>
export default {
  email: "",
  password: "",
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods: {
    clickit() {
      console.log("click");
      console.log(this.email, "email", this.password, "password");
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
input {
  margin: 10px;
  display: block;
}
button {
  display: block;
}
</style>
