<template>
  <div class="home">
    <Demo01></Demo01>
  </div>
</template>

<script lang="ts">
import Demo01 from "@/components/demo01/index.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Index",
  components: {
    Demo01,
  },
});
</script>
