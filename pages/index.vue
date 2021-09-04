<template>
  <div>
  </div>
</template>

<script>
import cartModule from '../components/cartModule.vue'
export default {
  components: {
    cartModule
  },

 data() {
   return {
   
  
         }
    }, 
  methods: {
    convertJson() {
       let newJson = '{"text":"овольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк","title":"a","price":12000,"href":"./img/Rectangle 31.jpg"}'
       let clone = JSON.parse(newJson)
       this.list.push(clone)
       console.log(this.list)
    }
  }
}
</script>


<style>

*{
  padding: 0;
  margin: 0;
  border: 0;
}
:focus, :active{outline: none;}
a:focus, a:active{outline: none;}

html,body{
  height: 100%; 
  width: 100%;
  font-size: 100%;
  line-height: 100%;
  font-size: 14px;
  -ms-text-size-adjust: 100%;
  -moz-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;

}
button{
  width: 100px;
  height: 100px;
  background-color: aqua;
}
  
</style>
