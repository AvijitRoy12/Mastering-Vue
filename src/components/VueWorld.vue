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
