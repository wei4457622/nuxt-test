<template>
  <div>
    <logo />
    <h1>{{title}}</h1>
    <h2>{{h2}}</h2>
    <h2 @click="demoFn">{{demoH2}}</h2>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import { sleep, deepCopy } from "~/assets/js/tool.js";
import * as tool from "~/assets/js/tool.js";
import test from "~/assets/js/test.js";

export default {
  data() {
    return {
      title: "demo",
      h2: "這是 h2"
    };
  },
  created() {
    test.test1("wei");
    console.log("created");
  },
  mounted() {
    console.log("mounted");
  },
  computed: {
    demoH2() {
      return this.h2 + "(computed)";
    }
  },
  methods: {
    demoFn() {
      console.log("demoFn");
    }
  },
  components: {
    Logo
  }
};
</script>
