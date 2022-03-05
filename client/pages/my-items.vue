<template>
  <div class="container">
    <MyItem v-for="myRental in myRentals" :key="myRental.id" :item="myRental" />
  </div>
</template>

<script>
import { mapState } from "vuex"
export default {
  layout: "no-nav",
  computed: {
    ...mapState(["myRentals"])
  }
}
</script>

<style lang="scss" scoped>
.container {
  padding: 5rem 0;
}
</style>
