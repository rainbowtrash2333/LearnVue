<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

</script>
<script>
// 声明式渲染，可以提高开发效率
export default {
  data() {
    return {
      num:0,
      uname:"Twikura"
    }
  }
}
</script>
<template>
  <div>
    <p>{{ num }}</p>
    <p>{{ uname }}</p>
  </div>
</template>

<style scoped>

</style>
