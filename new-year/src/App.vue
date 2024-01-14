<template>
<input type="text" v-model="name"><br><br>
<button @click="change">{{ visible == false ? "получить поздравление" : "спрятать поздравление" }}</button>
<p v-if="visible">{{ 'Поздравляю с новым годом, ' + name }}</p><br><br>
<input type="text" v-model="msg">
<ul>
  <li v-for="item, index in arr" :key="index">{{ item }}</li>
</ul>
<button @click="add">добавить пункт списка</button>
</template>

<script>
export default {
  data(){
    return{
      name: '',
      visible: false,
      arr: ['что','как','когда',],
      msg: '',
    }
  },
  methods:{
    change(){
      this.visible = !this.visible
    },
    add(){
      /* this.arr.push(this.msg) певрый номер*/
      this.arr.unshift(this.msg)
    }
  }
}
</script>

<style>

</style>
