<!--liyabin <liyabin@baidu.com> 2019-05-02-->

<template>
    <footer>
        <p>{{ copyright }} ------{{ title }}</p>
    </footer>
</template>
<script>
    export default {
        name:'app-footer',
        props:{
          title:{
              type:String
          }
        },
        data(){
            return{
                copyright:"Copyright 2019 Vue Demo"
            }
        },
        methods:{
        }

    }
</script>
<style scoped>
    footer{
        background-color: lightseagreen;
        padding: 6px;
    }
    p{
        color: blue;
        text-align: center;
    }
</style>
