<template>
    <div>
    <cart-module :list="list" />
    <button @click='convertJson'>new Json</button>
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
                {img: 'https://img.yakaboo.ua/media/catalog/product/cache/1/image/398x565/31b681157c4c1a5551b0db4896e7972f/i/m/img936_1_4.jpg', price:'1500', title:'Journey to the Center of the Earth', text:'описание', id: '/books/adventure/journey-to-the-center-of-the-planet svift'},
                {img: 'https://i.pinimg.com/originals/fb/e7/e9/fbe7e91768141703a7c2300c8f8e05a9.jpg', price:'1000', title:'Gulliver Travels', text:'описание', id: '/books/adventure/gulliver-travels'},
            ],
        }
    },
    methods: {
        convertJson() {
            let newJson = ['{"img":"https://i.pinimg.com/originals/fb/e7/e9/fbe7e91768141703a7c2300c8f8e05a9.jpg","price":"1000","title":"Gulliver Travels","text":"описание", "link": "/books/adventure/gulliver-travels"}',      
                           '{"img":"https://img.yakaboo.ua/media/catalog/product/cache/1/image/398x565/31b681157c4c1a5551b0db4896e7972f/i/m/img936_1_4.jpg","price":"1500","title":"Journey to the Center of the Earth","text":"описание", "link": "/books/adventure/journey-to-the-center-of-the-planet svift" }',
            ]
            for (let i = 0; i < newJson.length; i++) {
                let clone = JSON.parse(newJson[i])
                this.list.push(clone)
            }
    }   
    }
}
</script>

<style lang="sass" scoped>
  button
        width: 100px
        height: 100px
        position: absolute
        top: 100px
        left: 700px
</style>