<template>
  <div class="about">
    <h1>{{msg}}</h1>
    <button @click="pop">点击</button>
    <HelloWorld></HelloWorld>
    <el-button type="primary">主要按钮</el-button>

  </div>
</template>
<script>
import HelloWorld from '../components/HelloWorld'
export default {
  name: 'about',
  components: {
    HelloWorld,
  },
  data() {
    return {
      msg: 'hello will!'

    }
  },
  methods: {
    pop() {
      alert('hello lili')
    }
  }
}
</script>
