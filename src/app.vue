<template>
    <!-- <MyButton></MyButton> -->   
    <div class="container">
        <Header></Header>
        <Add :addComment="addComment"></Add>
        <List :coms="comments" :deleteComment="deleteComment"></List>
    </div> 
</template>

<script>
// import MyButton from '@/components/MyButton'
// import MyButton from './components/MyButton/MyButton.vue'
import Header from './components/Header'
import Add from './components/Add'
import List from './components/List'


export default {
  name: '',
  components:{
      // MyButton:MyButton
      Header:Header,
      Add,
      List,
  },
  data(){
    return {
      comments:[
        {id:1,content:'vue不错',username:'刘向阳'},
        {id:2,content:'诶呦,不错哦',username:'谢可寅'},
        {id:3,content:'你敢相信吗? 真不错!',username:'韦俊霞'},
      ]
    }
  },
   methods: {
    addComment(comment){
      this.comments.unshift(comment)
    },
    deleteComment(index){
      this.comments.splice(index,1)
    }
  },
}
</script>

<style scoped>

</style>
