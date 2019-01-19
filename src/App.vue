<template>
  <div id="app">
    <p>
      <router-link to='/'>Home</router-link>
      <router-link to='/player/1'>库里</router-link>
       <router-link to='/player/2'>哈登</router-link>
    </p>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>

</style>
