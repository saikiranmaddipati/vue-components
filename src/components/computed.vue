<template>
  <div class="hello">
    <h1>Methods</h1>
    <button v-on:click="a++">Add to A</button>
    <button v-on:click="b++">Add to B</button>
    <p>Age + A = {{ addToAcomputed }}</p>
    <p>Age + B = {{ addToBcomputed }}</p>
    <h1>{{ now() }}</h1>
  </div>
</template>

<script>
export default {
  name: "ComputedProps",
  data() {
    return {
      a: 0,
      b: 0,
      age: 20,
    };
  },
  methods: {
    now: function () {
      console.log("saikiran");
    },
  },
  computed: {
    addToAcomputed: function () {
      console.log("addToAcomputed");
      return this.a + this.age;
    },
    addToBcomputed: function () {
      console.log("addToBcomputed");
      return this.b + this.age;
    },
  },
};
</script>
