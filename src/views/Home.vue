<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Left :list="list" @changeind="change"/>
    <Right :list="list[ind].arr"/>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import Left from '@/components/left.vue';
import Right from '@/components/right.vue'
export default {
  name: 'home',
  data(){
    return {
      list:[
        {
          name:'哈哈哈',
          arr:[
            {
              id:'1',
              text:'大飞',
              num:1
            },
            {
              id:'2',
              text:'大红',
              num:2
            }
          ]
        },
         {
          name:'代发价',
          arr:[
            {
              id:'1',
              text:'未多少',
              num:1
            },
            {
              id:'2',
              text:'总共的',
              num:2
            }
          ]
        }
      ]
    }
  },
  components: {
    // HelloWorld
    Left,
    Right
  }
}
</script>
