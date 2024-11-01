<template>
  <div class="card mb-5">
    <div class="card-img-top bg-secondary text-white w-100 p-5 text-center card_img">{{ cardImgDescription }}</div>
    <div class="card-body">
      <h5 class="card-title p-2">{{ cardTitle }}</h5>
      <p class="card-text p-3">{{ cardText }}</p>
      <button type="button" class="btn btn-primary mx-2" @click="showModal()">
        Подробнее
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",

  props: {
    cardImgDescription: {
      type: String,
      required: true,
    },
    cardTitle: {
      type: String,
      required: true
    },
    cardText: {
      type: String,
      required: true
    },
    cardDetailedDescription: {
      type: String,
      required: true
    }
  },

  methods: {
    showModal() {
      this.$bvModal.msgBoxOk(`Подробная информация: \n${this.cardDetailedDescription}`);
    },
  },
}
</script>

<style scoped>

.card_img {
  width: 18rem;
  height: 18rem;
}
</style>