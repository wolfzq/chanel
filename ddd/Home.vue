<template>
  <div>
    <div v-for="(item,i) of list" :key="i">
       <li>item.laotop_id</li>
       <!-- <button @click="todetail(i)">详情</button> -->
       <router-link :to="{path:'/picture',query:{pic_id:item.pid}}">详情页</router-link>
    </div>
  </div>
</template>
<script>
export default {
  data(){
    return{
      list:[{"pid":2,"laptop_id":3,"sm":"img/product/sm/57b12a31N8f4f75a3.jpg","md":"img/product/md/57b12a31N8f4f75a3.jpg","lg":"img/product/lg/57b12a31N8f4f75a3.jpg"},{"pid":8,"laptop_id":3,"sm":"img/product/sm/57ad359dNd4a6f130.jpg","md":"img/product/md/57ad359dNd4a6f130.jpg","lg":"img/product/lg/57ad359dNd4a6f130.jpg"},{"pid":9,"laptop_id":3,"sm":"img/product/sm/57ad8846N64ac3c79.jpg","md":"img/product/md/57ad8846N64ac3c79.jpg","lg":"img/product/lg/57ad8846N64ac3c79.jpg"}]
    }
  },
  methods:{
    todetail(i){
      this.$router.push({path:`/Details/${i}`})
    }
  }
}
</script>