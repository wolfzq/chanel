<template>
  <div>
    详情
  </div>
</template>
<script>
export default {
  // props:{
  //   "lid":"sting"
  // },
  data(){
    return{
      data:[]
    }
  },
  mounted(){
    let  lid=this.$router.query.pic_id;
    let  url="http://localhost:4000/picture"
    this.axios.get(url,{params:lid}).then(res=>{
      console.log(result)
      
    })
  }

}
</script>