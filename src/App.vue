<script setup>
// import Content from "./components/Content.vue";
// import Backgroundicon from "./components/backgroundicon.vue";
const textTitle = import.meta.env.VITE_TEXT_TITLE;
const textContent = import.meta.env.VITE_TEXT;

import ICPInfoFooter from "./components/ICPInfoFooter.vue";
</script>

<template>
<!-- <Content></Content>
  <backgroundicon></backgroundicon> -->

    <div class="card">
      <h3>{{ textTitle }}</h3> {{ textContent }}
    </div>

  <ICPInfoFooter></ICPInfoFooter>
</template>

<style>
@property --a {
  syntax: "<angle>";
  initial-value: 0deg;
  inherits: false;
}

.card {
  overflow: hidden;
  position: relative;
  width: min(12.5em, 80vmin);
  aspect-ratio: 1;
  border-radius: 0.5em;
  place-self: center;
  place-content: center;
  padding: 0.5em;
  color: #ededed;
  font: clamp(1em, 2vw + 2vh, 2em) sans-serif;
  text-align: center;
  text-transform: uppercase;
  text-wrap: balance;
}
.card::before {
  position: absolute;
  z-index: -1;
  inset: -1em;
  border: solid 1.25em;
  border-image: conic-gradient(from var(--a), #669900, #99cc33, #ccee66, #006699, #3399cc, #990066, #cc3399, #ff6600, #ff9900, #ffcc00, #669900) 1;
  filter: blur(0.75em);
  animation: a 4s linear infinite;
  content: "";
}
@keyframes a {
  to {
    --a: 1turn;
  }
}

html,
body,
div {
    display: grid;
}

html {
    min-height: 100%;
}

body {
    background: url(https://images.unsplash.com/photo-1753165119932-b5af9e084c77?w=1400) 50%/cover #212121;
    background-blend-mode: multiply;
    grid-template-rows: 1fr auto;
    min-height: 100vh;
    margin: 0;
    color: #ededed;
}
</style>