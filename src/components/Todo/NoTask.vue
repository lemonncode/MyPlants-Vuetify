<template>
  <div class="no-tasks">
    <v-icon class="icon" size="85" color="blue darken-6">
      mdi-cart-heart
    </v-icon>
    <div class="text-h5 primary--text">No hay plantitas</div>
  </div>
</template>

<script>
export default {};
</script>
<style lang="sass">
.no-tasks
  position: absolute
  left: 50%
  top: 50%
  transform: translate(-50%, -50%)
  opacity: 0.5
.icon
  position: relative
  left: 25%
  top: 50%
</style>