<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup

</script>
<script>
// 声明式渲染，可以提高开发效率
export default {
  data() {
    return {
      num:0,
      uname:"Twikura",
      message:"<h2>Title</h2>",
      id:'id0',
      url:"https://v3.cn.vuejs.org/logo.png",
      attributeName:'id',
      mouseEvent:'click',
      message2:"Hello  the World"
    }
  },
  methods:{ //给Vue定义了方法
    changeUmane:function () {
      this.uname = "Rainbow Trash"
    },
    changeId:function () {
      this.id = this.id.substring(0, 2) + ((parseInt(this.id.substring(2)) + 1) % 2)
    }
  },
  computed:{
    reverseMsg2:function (){
      return this.message2.split('').reverse().join('')
    }
  }
}
</script>
<template>
  <div>
    <p>{{ num }}</p>

    <p>{{ uname }}</p>
    <p v-once>{{ uname }}</p>
    <button @click="changeUmane">改变名字</button>

    <p>{{ message }}</p>
    <p v-html="message"></p>

    <!--    动态绑定属性-->
    <p v-bind:id="id"> v-bind绑定</p>
    <button @click="changeId">循环改变id</button>
    <button @click="id='id1'">改变id</button>

    <img v-bind:src="url" alt="">

    <p>{{ num + 1 }}</p>
    <p>{{ uname.split('').reverse().join('') }}</p>

    <p :id="id">test</p>
    <!--    监听事件-->
    <button v-on:click="changeId">监听事件</button>
    <!--    动态参数-->
    <!--    动态属性-->
    <p v-bind:[attributeName]="id"> v-bind绑定</p>
    <button @[mouseEvent]="attributeName='class'">Change Attribute</button>
    <button @click="mouseEvent='mouseover'">Change Enven</button>

<!--    计算属性-->
    <p>{{reverseMsg2}}</p>
  </div>
</template>

<style>
#id0 {
  background: rosybrown;
  font-size: large;
  font-weight: bolder;
  color: red;
}

#id1 {
  color: blue;
}

.id0 {
  color: red;
  font-size: 50px;
}

</style>
