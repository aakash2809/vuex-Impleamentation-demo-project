<template>
  <div>
    <!--  <h1>{{ msg }}</h1>
    <h2>{{ data }}</h2> -->
    <button>call hello function</button>
  </div>
</template>
<script>
export default {
  name: "Home",
  props: {
    msg: String,
    data: String,
  },
  methods: {
    hello() {
      console.log("");
    },
  },
};
</script>