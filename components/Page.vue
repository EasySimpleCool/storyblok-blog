<template>
  <div v-editable="blok" class="page">
    <div v-editable="blok" class="postimage">
      <img :src="blok.image"> 
    </div>
    <component :key="blok._uid" v-for="blok in blok.body" :blok="blok" :is="blok.component"></component>
  </div>
</template>

<script>
export default {
  props: ['blok']
}
</script>

<style scoped>
.page {
  display: grid;
  grid-gap: 8px;
  background-color: #ffffff;
  border-radius: 8px;
  padding: 8px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
}

img {
  width:100%;
  height: auto;
  border-radius: 4px;
  object-fit: cover;
  background-color: none;
}
</style>
