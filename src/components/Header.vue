<!--liyabin <liyabin@baidu.com> 2019-05-02-->


<template>
    <header>
        <h1 @click="deleteStr"> {{ title1 }}  ---------{{ title }}</h1>
    </header>
</template>

<script>
    export default {
        name: "app-header",
        props:{
            title:{
                type:String,
            }
        },
        data(){
            return {
                title1:"Vue.js Demo",
                children:"子组件向父组件传值"
            }
        },
        methods:{
            deleteStr(){
                // this.title = "changed";
                // 子组件通过this.$emit()的方式将值传递给父组件,titleChanged是父组件中绑定的函数名
                this.$emit("titleChanged",this.children);
            }
        }
    }
</script>

<style scoped>
header{
    background-color: lightseagreen;
    padding: 10px;
}
    h1{
        color: #222;
        text-align: center;
    }
</style>