<template>
  <div ref="dom"></div>
</template>

<script lang="ts">
import { defineComponent, onMounted, ref } from "vue";
import * as THREE from "three";

export default defineComponent({
  name: "Demo01",
  setup() {
    const dom: any = ref(null);

    onMounted(() => {
      const scene = new THREE.Scene();
      const camera = new THREE.PerspectiveCamera(
        75,
        window.innerWidth / window.innerHeight,
        0.1,
        1000
      );
      const renderer = new THREE.WebGLRenderer();
      renderer.setSize(window.innerWidth, window.innerHeight);
      if (dom.value) {
        dom.value.appendChild(renderer.domElement);
      }
    });
    return {
      dom,
    };
  },
});
</script>
