<template>
  <div>
    <ul>
      {{
        i
      }}
      <nuxt-link
        :to="{
          name: 'detail-indexs',
          params: { id: i },
        }"
      ></nuxt-link>
    </ul>
  </div>
</template>
<script>
export default {}
</script>
<style></style>
