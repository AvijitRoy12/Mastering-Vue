<template>
  <h1>{{ context }}</h1>
  <hr />
  <h3 v-if="show">If show is true then I am displayed</h3>
  <h3 v-else>If show is not true then I am displayed</h3>
  <button v-on:click="show = !show">Toggle</button>
</template>

<script>
export default {
  name: "ConditionalRendering",
  data() {
    return {
      context: "I render the context conditionally",
      show: true,
    };
  },
  methods: {},
};
</script>
