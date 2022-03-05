<template>
  <div class="review-card">
    <div class="image-container">
      <img :src="reviewer.picture.large" alt="reviewer image">
    </div>
    <div class="text-container">
      <h6>
        {{ reviewer.login.username }}
      </h6>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur eos
        inventore eveniet tempore optio et laboriosam aliquid accusantium, illo
        tenetur quaerat repellat assumenda ipsum ex. Quaerat ad corporis libero
        aperiam.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    reviewer: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style lang="scss" scoped>
.review-card {
  margin-top: 1.5rem;
  height: 4rem;
  display: flex;

  img {
    width: 4rem;
    height: 4rem;
    border-radius: 100%;
  }

  p {
    color: gray;
  }

  .text-container {
    margin-left: 2rem;
  }
}
</style>
