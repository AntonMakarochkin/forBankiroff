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
                {img: 'https://images.biggeek.ru/1/435/a39e/11042-365grey_20_min.jpg', price:'50000', title:'Samsung S20', text:'описание', id: '/phones/android/samsungs20'},
                {img: 'https://images.biggeek.ru/1/435/effd/10902-551ru-galaxy-a51-a515-sm-a515fzkmser-front-199712181.jpeg', price:'25000', title:'Samsung A5', text:'описание', id: '/phones/android/samsunga5'},
            ],
        }
    },
}
</script>