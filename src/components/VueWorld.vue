<template>
  <h1>This is vue world</h1>
  <p>{{ message }}</p>
  <h2>{{ usage() }}</h2>
  <h2>Package manager: {{ packageManager() }}</h2>
  <hr />
  <h1>Developer details</h1>
  <h3>Name: {{ address().name }}</h3>
  <h3>Address: {{ address().address }}</h3>
  <h3>Phone: {{ address().phone }}</h3>
  <hr />
  <div id="main">
    <div id="left">Name: {{ getName("Avijit Roy") }}</div>
    <div id="right">
      <p>Phone number: {{ getPhoneNumber(12345) }}</p>
      <p>Message: {{ getMessage() }}</p>
    </div>
  </div>
  <hr />
  <button v-on:click="clickTest()">Click me</button>
  <button v-on:dblclick="doubleClickTest()">Click me</button>
  <h2>{{ count }}</h2>
  <hr />
  <input type="text" v-model="count" />
  <h2>{{ count }}</h2>
  <hr />
  <input type="text" placeholder="Email" v-model="email" />
  <input type="password" placeholder="Password" v-model="password" />
  <button v-on:click="getDetails()">Submit</button>
</template>
<script>
export default {
  name: "VueWorld",
  data() {
    return {
      message: "This is a framework based on JavaScript",
      count: 0,
      email: null,
      password: null,
      usage: function () {
        return "Frontend development for complex web applications";
      },
      packageManager: function () {
        return "Node package manager";
      },
      address: function () {
        return {
          name: "Avijit Roy",
          address: "Reichenhainer Str",
          phone: 12345533,
        };
      },
    };
  },
  methods: {
    getName(name) {
      return name;
    },
    getPhoneNumber(phone) {
      return phone;
    },
    getMessage() {
      return this.message;
    },
    clickTest() {
      return this.count++;
    },
    doubleClickTest() {
      return alert("Button is double clicked");
    },
    getDetails() {
      console.log(`Name: ${this.email} Password: ${this.password}`);
    },
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
h3 {
  color: lightseagreen;
}
#main {
  width: 100%;
  height: 300px;
  position: relative;
  display: flex;
}
#left {
  width: 50%;
  height: 300px;
  line-height: 300px;
  text-align: center;
  background-color: antiquewhite;
}
#right {
  width: 50%;
  height: 300px;
  text-align: center;
  background-color: crimson;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

#right p {
  margin: 0;
  line-height: normal;
  padding: 10px;
  color: white;
}
</style>
