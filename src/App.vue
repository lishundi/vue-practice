<template>
  <div>
    <!--应用-->
    <!--<app-header :title="title" @titleChanged="updateTitle($event)"></app-header>-->
    <!--&lt;!&ndash;从父组件向子组件传值就使用属性：自定义属性users&ndash;&gt;-->
    <!--<app-results :users="users"></app-results>-->
    <!--<app-results :users="users"></app-results>-->
    <!--<app-footer :title="title"></app-footer>-->
    <!--从父组件向子组件传值就使用属性：自定义属性users和title-->
    <Header :title="title" @titleChanged="updateTitle($event)"/>    <!--$event中是子组件传过来的数据-->
    <Results :users="users"/>
    <Results :users="users"/>
    <Footer :title="title"/>
  </div>
</template>

<script>
  // 导入
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import Results from './components/Users.vue';
  export default {
    // 注册
    components: {
      // 'app-header':Header,
      // 'app-footer': Footer,
      // 'app-results': Result,
      Header,
      Footer,
      Results
    },
    data () {
      return {
        users: [
          {name: 'Ryu', speciality: 'Vue Components', show: false},
          {name: 'Crystal', speciality: 'HTML Wizardry', show: false},
          {name: 'Hibachi', speciality: 'Click Events', show: false},
          {name: 'Tango', speciality: 'Conditionals', show: false},
          {name: 'Kali', speciality: 'Webpack', show: false},
          {name: 'Yoshi', speciality: 'Data Diggings', show: false},
          {name: 'Lassa', speciality: ' Lara Diffs', show: false}
        ],
        title:"这是传值方式(Number,String,Boolean)"

      }
    },
    methods:{
      updateTitle(data){
        this.title = data;
      }
    }
  }
</script>

<style>
  body{
    margin: 0;
    font-family: 'Nunito SemiBold',serif;
  }
</style>
