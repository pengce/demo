<script setup lang="ts">
import Button from './components/Button.vue'
import HelloWorld from './components/HelloWorld.vue'
import { reactive, ref } from 'vue';

const state = reactive({ count: 0 })
const count = ref('123');
const books = ref<any[]>();
const info = ref({ title: '点击', type: 'primary' })
console.log("buttonInfo", info)
const getInfo = (e) => {
  console.log(e);
}
const ggg = (e) => {
  console.log(e)
}
</script>

<template>
  <div>
    <Button :buttonInfo="info" @getInfo="getInfo" @ggg="ggg"></Button>
    <!-- <Button :test="buttonInfo"></Button> -->
    <button @click="state.count++">{{ state.count }}</button>
    <button @click="count++">{{ count }}</button>
  </div>
  <div>
    {{ books && books.length }}
    姓名： <span>{{ books?.length ? '123' : '无' }}</span>
  </div>
  <HelloWorld msg="Vite + Vue" />
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
