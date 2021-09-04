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
                {img: 'https://img4.labirint.ru/rc/b403db3382fb5bda3f344f0c8adf9d3c/220x340/books49/488632/cover.jpg?1612689915', price:1500, title:'War and Peace', text:'описание', id: '/books/classic/war-and-peace',   },
                {img: 'https://cv7.litres.ru/pub/c/elektronnaya-kniga/cover_max1500/24312573-ivan-turgenev-otcy-i-deti-24312573.jpg', price:1000, title:'Fathers and Sons', text:'описание', id: '/books/classic/fathers-and-sons'},
            ],
        }
    },
    methods: {
        convertJson() {
            let newJson = ['{"img":"https://img4.labirint.ru/rc/b403db3382fb5bda3f344f0c8adf9d3c/220x340/books49/488632/cover.jpg?1612689915","price":1500,"title":"War and Peace","text":"описание", "id": "/books/classic/fathers-and-sons" }',      
                           '{"img":"https://cv7.litres.ru/pub/c/elektronnaya-kniga/cover_max1500/24312573-ivan-turgenev-otcy-i-deti-24312573.jpg","price":1000,"title":"Fathers and Sons","text":"описание", "id": "/books/classic/fathers-and-sons" }',
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