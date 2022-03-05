<template>
  <div class="item-container">
    <img :src="require(`@/assets/images/${item.image}`)" alt="">
    <div class="text-container">
      <h4>
        {{ item.title }}
      </h4>
      <p>
        {{ item.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style lang="scss" scoped>
.item-container {
  display: flex;
  margin: 3rem 0;

  img {
    width: 30%;
    object-fit: cover;
    height: 100%;
    border-radius: 0.5rem;
  }

  p {
    font-size: 0.8rem;
    color: gray;
  }

  .text-container {
    padding: 0 1rem;
  }
}
</style>
