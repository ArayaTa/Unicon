<template>
  <div>
    <ul>
      {{
        i
      }}
      <nuxt-link
        :to="{
          name: 'detail-index',
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
