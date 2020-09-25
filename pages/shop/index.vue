<template>
    <div>
    <h1>Shop Page </h1>
    <ul>
       <li v-for="i in 10" :key="i">สินค้าหมายเลข {{ i }}
      <nuxt-link :to="{ name: 'shop-id', params: { id: i}}"> รายละเอียด </nuxt-link> 
       
       </li>
    
    </ul>
    
    
    
    
    
    </div>
</template>

<script>
export default {
    
}
</script>