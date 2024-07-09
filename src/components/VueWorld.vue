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
    <div id="left">left</div>
    <div id="right">right</div>
  </div>
</template>
<script>
export default {
  name: "VueWorld",
  data() {
    return {
      message: "This is a framework based on JavaScript",
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
};
</script>

<style scoped>
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
  line-height: 300px;
  text-align: center;
  background-color: crimson;
}
</style>
