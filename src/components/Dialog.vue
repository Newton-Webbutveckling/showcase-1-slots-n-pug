<template lang="pug">
  article
    slot(name="heading")
      h1 Heading
    slot(name="content")
      p Lorem ipsum dolor sit amet consectetur
    button OK
    button(@click="$emit('cancel')") Cancel
</template>

<script>
export default {

}
</script>

<style scoped lang="sass">
article
  background-color: white
  padding: 2rem
  border-radius: 5px

  p
    color: hotpink


</style>