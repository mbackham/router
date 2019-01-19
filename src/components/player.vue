<template>
    <div>
        <h1>球员页面</h1>
        <p>{{detail}}</p>
  </div>
</template>
<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      detail:{}
    }
  },
  mounted () {
    this.detail= this.getPlayer(this.$route.params.uid)
  },
  beforeRouteUpdate(to, from, next) {//记录着你这个路由从哪里来，到哪里去
    this.detail=this.getPlayer(to.params.uid)
    next()
  },
  methods: {
      getPlayer(uid){
    switch(uid){
      case '1':
      return{uid:1, name:'库里',point:26};
      case '2':
      return{uid:1, name: '哈登',point:30};
      default:
      return{
        uid:-1 
      }
    }
  }
  }
  
}
</script>
<style>

</style>
