<template>
  <div id="vue_det">
    <h1>site: {{site}}</h1>
    <h1>url: {{url}}</h1>
    <h1>{{details()}}</h1>
    <div v-show="aa">1111111121222</div>
    <div v-if="aa">999999999</div>
    <p v-html="message"></p>
    <pre><a v-bind:href="url">菜鸟教程</a></pre>
    <pre><a :href="urle">菜鸟教程</a></pre>
    <pre><a @click="myC">菜鸟教程</a></pre>
    <p>{{message1}}</p>
    <input v-model="message1">
    <p>{{message2}}</p>
    <button v-on:click="reverseMessage">反转字符串</button>
    {{message3 | capitalize}}
    <div v-bind:id="rawId | formatId"></div>
  </div>
</template>
<script type="text/javascript">
export default {
  data () {
    return {
      site: '菜奶交代',
      url: 'wwww.baidu.con',
      alexa: '10000',
      message: '<b>错误了</b>',
      aa: true,
      urle: 'http:wwww.baidajfjasdf.com',
      message1: '测试',
      message2: '1234567890',
      message3: 'hello word',
      rawId: '9999'
    }
  },
  filters: {
    capitalize: function (value) {
      if (!value) return ''
      value = value.toString()
      return value.charAt(0).toUpperCase() + value.slice(1)
    },
    formatId: function (value) {
      if (!value) return ''
      value = value.toString()
      return value + '11112222'
    }
  },
  methods: {
    details: function () {
      return this.site + '-----ip afdjasdflalkjsdfaiosdfasdfhasdklhfk'
    },
    myC: function () {
      alert('aaaaaa')
    },
    reverseMessage: function () {
      this.message2 = this.message2.split('').reverse().join('')
    }
  }
}
</script>
