<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import MyForm from './components/MyForm.vue'
</script>

<template>
  <div>
    <!-- ACÁ mete los dos LOGOS básicamente nomás -->
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <!--  Hay "custom objects" de Vue como este Hellowrold-->
  <!-- con atributos propios de ellos -->
  <!-- Es el -->
  <!-- <HelloWorld msg=" TIENE DELAY IGUAL " /> -->
  <MyForm/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
