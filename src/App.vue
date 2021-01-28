<script>
import createPilingJs, { createImageRenderer } from "piling.js";

console.log('???');

export default {
  name: 'App',
  data() {
    console.log('a is: ')
    return {
      counter: 0
    }
  },
  methods: {
    initPiling: function () {
      createPilingJs(this.$refs.piling, {
        renderer: createImageRenderer(),
        items: [
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000253413.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000533739.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000314530.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000418512.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000454273.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000219654.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000558596.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000392493.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000115639.jpg' },
          { src: 'https://storage.googleapis.com/pilingjs/coco-cars/000000228398.jpg' },
        ],
        darkMode: true,
      });
    }
  },
  mounted: function () {
    this.initPiling()
  }
}
</script>

<style>
  #topbar {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 6rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 2rem;
  }
  #topbar a {
    color: white;
    text-decoration: none;
    box-shadow: inset 0 -2px 0 0 #808080;
    transition: 0.2s all ease;
  }
  #topbar a:hover {
    color: #ff7ff6;
    box-shadow: inset 0 -10px 0 0 #ff7ff6;
  }
  #piling {
    position: absolute;
    top: 6rem;
    left: 0;
    right: 0;
    bottom: 0;
    border-top: 1px solid #808080;
  }
</style>

<template>
  <header id="topbar">
    <p>
      This is
      <a
        href="https://github.com/flekschas/piling.js"
        target="_blank"
        rel="noopener noreferrer"
      >
        Piling.js
      </a>
      running in a
      <a
        href="https://v3.vuejs.org"
        target="_blank"
        rel="noopener noreferrer"
      >
        Vue.js 3
      </a>
      app.
    </p>
  </header>
  <div id="piling" ref="piling" />
</template>
