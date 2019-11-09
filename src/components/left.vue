<template>
    <div class="left">
        <ul>
            <li v-for="(item,index) in list" :key="index"
            @click="changeInd(index)">{{item.name}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    props:{
        list:{
            type:Array
        }
    },
    created(){
         console.log(this.list)
    },
    methods:{
        changeInd(ind){
            this.$emit('changeind',ind);
        }
    }
}
</script>

<style>

</style>