<template>
<div>
    <p class="title-task"></p>
    <button>bbfdbdfb</button>
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
         return this.todosNew.find(item => item.id == this.$route.params.id)
        }
     }
  }

</script>
