<template>
<div>
  <h1>I'm a PhotoComponent</h1>
  <h3 v-if="$route.params.id.length !== 0">My photo-id is {{$route.params.id}}</h3>
  <h3 v-else> I don't have parameter :c</h3>
</div>
</template>

<script>
export default {
name: "Photo"
}
</script>

<style scoped>

</style>