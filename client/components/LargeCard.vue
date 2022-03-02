<template>
  <div class="card">
    <img
      :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)"
      alt="fire extinguisher"
      class="image"
    >
    <h3 class="header">
      {{ card.title }}
    </h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    card: {
      type: Object,
      default: () => {
        return {}
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  border-radius: 1rem;
  overflow: hidden;
  padding: 0;
  cursor: pointer;

  .image {
    height: 65%;
    border-radius: 1rem 1rem 0 0;
  }

  .header, .snippet {
    padding: 0 1rem;
  }

  .header {
    font-size: 1.15rem;
    margin-top: 0.4rem;
  }

  .snippet {
    color: grey;
  }
}
</style>
