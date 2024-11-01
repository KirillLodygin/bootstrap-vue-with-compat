<template>
  <div class="body">
    <div class="ml-5 d-flex justify-content-center flex-wrap">
      <Card
          v-for="card in generateCardsData(8)"
          :card-detailed-description="card.cardDetailedDescription"
          :card-text="card.cardText"
          :card-title="card.cardTitle"
          :cardImgDescription="card.cardImgDescription"
      />
    </div>
  </div>
</template>

<script>
import Card from './Card.vue'

export default {
  name: "Body",

  components: {
    Card
  },

  methods: {
    generateRandomString(length) {
      let result = '';
      const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789';
      for (let i = 0; i < length; i++) {
        result += characters.charAt(Math.floor(Math.random() * characters.length));
      }
      return result;
    },

    generateCardsData(length) {
      const cardsData = []
      for (let i = 0; i < length; i++) {
        cardsData.push({
          cardImgDescription: `Изображение${i + 1}`,
          cardTitle: `Название карточки_${i + 1}`,
          cardText: this.generateRandomString(15),
          cardDetailedDescription: this.generateRandomString(45)
        })
      }
      return cardsData
    }
  }
}
</script>

<style scoped>
.d-flex{
  gap: 100px;
}
</style>