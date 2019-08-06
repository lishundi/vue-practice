<!--liyabin <liyabin@baidu.com> 2019-05-02-->
<template>
    <div id="users">
        <ul>
            <li v-for="item in users" @click="item.show = !item.show">
                 <h2>{{ item.name }}</h2>
                <h3 v-show="item.show">{{ item.speciality }}</h3>
            </li>
        </ul>
        <button @click="deleteObj">Delete</button>
    </div>
</template>
<script>
    export default {
        name:'app-users',
        // props:['users'],
        // 推荐使用
        props: {
            users: {
                type: Array,
                required: true
            }
        },
        data(){
            return{

            }
        },

        methods: {
            deleteObj () {
                this.users.pop();
            }
        }

    }
</script>
<style scoped>
    #users{
        width: 100%;
        max-width: 1200px;
        margin: 40px auto;
        padding: 0 20px;
        box-sizing: border-box;
        background-color: lightgreen;
    }
    ul{
        display: flex;
        flex-wrap: wrap;
        list-style-type: none;
        padding: 0;
    }
    li{
        flex-grow: 1;
        flex-basis: 300px;
        text-align: center;
        padding:  30px;
        border: 1px solid #222;
        margin: 10px;
        background-color: lightcoral;
    }
</style>
