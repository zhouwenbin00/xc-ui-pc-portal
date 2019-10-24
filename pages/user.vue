<template>
    <div>
      用户导航管理--user.vue，
      <nuxt-link :to="'/user/101'">修改</nuxt-link>
      <nuxt-child/>
    </div>
</template>

<script>
    export default {
        name: "user",
        layout: "test"
    }
</script>

<style scoped>

</style>
