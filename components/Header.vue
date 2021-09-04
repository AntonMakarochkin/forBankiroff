<template>
  <div>
    <div class="menu">
      <div class="menu__sector">
        <div>Books</div>
        <nuxt-link to='/books/classic'>classic</nuxt-link>
        <nuxt-link to='/books/adventure'>adventure</nuxt-link>
      </div>
      <div class="menu__sector">
        <div>Phones</div>
        <nuxt-link to='/phones/iphones'>iphone</nuxt-link>
        <nuxt-link to='/phones/android'>android</nuxt-link>
      </div>
    </div>

  </div>
</template>

<script>
export default {}
</script>


<style lang="sass" scoped>

  .menu
    width: 250px
    height: 400px
    font-size: 25px
    margin: 10px 30px
    box-shadow: 0px -1px 12px 5px rgba(34, 60, 80, 0.2)
    

    
  

  .menu__sector
    width: 150px
    height: 180px
    margin: 10px 30px
    display: flex
    flex-direction: column
    justify-content: space-around
    a
      margin: 0 0 0 10px
   
    
    
    
  .menu__link
    margin: 0 0 0 20px
  

  
    
  
  
</style>
