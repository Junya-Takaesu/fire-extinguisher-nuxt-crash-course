<template>
  <div>
    <b-button id="show-btn" @click="showModal">Rent</b-button>

    <b-modal ref="my-modal" hide-footer title="Using Component Methods">
      <div class="calendar-container">
        <div class="text-container">
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Eum, architecto debitis soluta possimus mollitia dolores repellat omnis cupiditate dolor quasi ad dolore est tempora id provident, sint expedita saepe odio sapiente nobis autem neque harum itaque numquam? Pariatur, similique nemo?</p>
        </div>
        <vc-date-picker color="red" :value="null" :is-range="true" />
      </div>
      <b-button id="show-btn" variant="outline-danger" @click="() => addItem(product.id)">Order</b-button>
    </b-modal>
  </div>
</template>

<script>
import { mapMutations } from "vuex"
export default {
  props: {
    product: {
      type: Number,
      default: () => null
    }
  },
  methods: {
    showModal() {
      this.$refs["my-modal"].show()
    },
    hideModal() {
      this.$refs["my-modal"].hide()
    },
    toggleModal() {
      // We pass the ID of the button that we want to return focus to
      // when the modal has hidden
      this.$refs["my-modal"].toggle("#toggle-btn")
    },
    ...mapMutations(["addItem"])
  }
}
</script>

<style lang="scss" scoped>
button {
  width: 100%;
  border: none;
  padding: 0.5rem;
  font-weight: 700;
  padding: 1rem 4rem;
  border-radius: 1rem;
  background: rgb(231, 81, 43);
  transition: 0.5s;
  color: white;
}
.calendar-container {
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}
p {
  color: gray;
}
.text-container {
  padding: 0.5rem;
}
</style>
