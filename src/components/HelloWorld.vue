<template>
  <h1 v-for="s in inp" :key="s">1{{ s }}</h1>
  <div>
    <form action="" @submit.prevent="clickit">
      <custom-input label="gmail" v-model="email" placeholder="Gmail" />
      <custom-input
        label="password"
        v-model="password"
        placeholder="Password"
      />
      <p v-for="str in inputs" :key="str">{{ str }}</p>

      <button>Login</button>
    </form>
  </div>
</template>

<script>
import CustomInput from "./Custom-Input.vue";
export default {
  components: {
    CustomInput,
  },
  props: {
    msg: String,
  },
  methods: {
    clickit() {
      console.log("click");
      console.log(this.email, "email", this.password, "password");
    },
  },
  data() {
    return {
      email: "",
      password: "",
      name: "HelloWorld",
      inp: ["email", "password", "name"],
    };
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
