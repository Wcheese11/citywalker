<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <!--<HelloWorld/>-->
    <input v-model="inputValue">
    <button @click="handleSubmit">提交</button>
    <ul>
      <todoitem :key= index v-for="(item,index) in list"
      :content="item"
      :index="index"
      @delete="handleDelte">
      </todoitem>
    </ul>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
//
// export default {
//   name: 'todolist',
//   components: {
//     HelloWorld
//   }
// }

import todoitem from './todoitem'// 引入组件
export default {
  components: {
    'todoitem': todoitem // 注册导入的组件作为标签使用
  },
  data () { // 声明返回的数据，跟实例data一样的作用，只是写法不同
    return {
      inputValue: '',
      list: []
    }
  },
  methods: {
    handleSubmit () {
      this.list.push(this.inputValue)
      this.inputValue = ' '
    },
    handleDelte (index) {
      this.list.splice(index, 1)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
