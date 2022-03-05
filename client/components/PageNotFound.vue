<template>
  <div>
    <h1>Page Not Found</h1>
    <img
      :src="require('@/assets/images/fe25.jpg')"
      alt="Sad fire extinguisher"
    >
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
div {
  padding: 7rem 0;
  display: flex;
  align-items: center;
  justify-content: center;

  h1 {
    font-size: 7.5rem;
  }

  img {
    width: 15rem;
    margin: 0 auto;
  }
}
</style>
