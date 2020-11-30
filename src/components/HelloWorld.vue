<template>
  <ul>
    <li v-for="(item, index) in list" :key="index"></li>
  </ul>
</template>

<script>
import axios from "axios";
export default {
  name: "HelloWorld",
  data() {
    return {
      list: []
    };
  },
  mounted() {
    axios.get("http://localhost:3000/list").then(res => {
      console.log(res);
    });
  }
};
</script>
