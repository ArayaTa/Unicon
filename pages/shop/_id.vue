<template>
<div>
   <h1>รายละเอียด</h1>
   <h2>สินค้าหมายเลข {{ this.$route.params.id}}</h2>
   <h3>{{ id }}</h3>

</div>

    
</template>
<script>
export default {
    data(){
        return {
            id: this.$route.params.id,
        }
    },
}
</script>
<style></style>