<template>
<div v-bind="rr">
  <router-link to="/todos">Перейти к списку</router-link>
    <p class="title-task">{{filt.title}}</p>
    </div>
</template>
<script>


export default {

    data(){
        return{
            todosNew:[],
            filt:""
        }
    },
    mounted(){
   if (localStorage.getItem('todos')) {
      this.todosNew = JSON.parse(localStorage.getItem('todos'));
    }
  },
   computed:{
     rr(){
         return this.todosNew.find((item) => {
          if(item.id == this.$route.params.id){
            return this.filt = {...item}
          }
     })
        }
     }
  }

</script>
