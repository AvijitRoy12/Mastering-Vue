<template>
  <h1>This is vue world</h1>
  <h1>My name is {{ name }}</h1>
</template>
<script>
export default {
  name: "VueWorld",
  data() {
    return {
      name: "Avijit",
    };
  },
};
</script>
