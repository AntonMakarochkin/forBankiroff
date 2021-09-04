<template>
    <div>
       <cart-module :list="list" />

    </div>
</template>
<script>
import cartModule from '../../../components/cartModule.vue'
export default {
    components: {
      cartModule  
    },
    
    data() {
        return {
             list: [
                {img: 'https://images.biggeek.ru/1/435/4347/7220-721xsmax_silver.jpg', price:'60000', title:'Iphone10', text:'описание', id: '/phones/iphones/iphone10'},
                {img: 'https://images.biggeek.ru/1/435/54e3/3217-1727_rose.jpg', price:'45000', title:'Iphone6', text:'описание', id: '/phones/iphones/iphone6'},

                
            ],
        }
    },
}
</script>

<style lang="sass" scoped>
    img
        width: 100%
        height: 100px
        object-fit: cover
</style>