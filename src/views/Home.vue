<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <hot-table :data="data" :rowHeaders="true" :colHeaders="true"></hot-table>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import { HotTable } from "@handsontable/vue";

export default {
  name: "Home",
  data: function () {
    return {
      data: [
        ["", "Ford", "Volvo", "Toyota", "Honda"],
        ["2016", 10, 11, 12, 13],
        ["2017", 20, 11, 14, 13],
        ["2018", 30, 15, 12, 13],
      ],
    };
  },
  components: {
    HelloWorld,
    HotTable,
  },
};
</script>

<style src="../node_modules/handsontable/dist/handsontable.full.css"></style>