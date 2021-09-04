<template>
    <div>
       <div class="cart" v-for='(item, index) in list' :key="index" >
           <div class="img">
                <nuxt-link :to='item.id'>
                      <img v-bind:src="item.img" alt="">
                </nuxt-link>
            </div>
           <div class="price">{{item.price}}</div>
           <div class="title">{{item.title}}</div>
           <div class="description">{{item.text}}</div>
           
          
       </div>
    </div>
</template>

<script>
export default {
    props: {
        list: Array,
    }
   
}
</script>

<style lang="sass" scoped>
    .cart
        width: 300px
        height: 300px
        box-shadow: 0px -1px 12px 5px rgba(34, 60, 80, 0.2)
        margin: 20px 20px 
        position: relative
        top: -420px
        left: 300px

        
    .price
        width: 100%
        height: 30px
        margin: 0 0 0 15px
   .title
        width: 100%
        height: 30px
        margin: 0 0 0 15px

   .description
        width: 100%
        height: 30px
        margin: 0 0 0 15px

   .img
        width: 100%
        height: 200px
        img
          width: 100%
          height: 100%
          object-fit: contain
   
                                
        
</style>