<template>
  <div id="app">
    <p> Your tarot of the day is... </p>
    <img :src="'https://www.sacred-texts.com/tarot/pkt/img/'+ cardData.name_short +'.jpg'" />
    <p><strong>{{cardData.name}}</strong></p>
    <p>{{cardData.meaning_up}}</p>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      cardData: null,  
    }
  },

  // Fetches posts when the component is created.
    created() {
      axios.get(`https://rws-cards-api.herokuapp.com/api/v1/cards/random?n=1`)
      .then(response => {
        // JSON responses are automatically parsed.
        this.cardData = response.data.cards[0]
      })
      .catch(e => {
        this.errors.push(e)
      })
    }
  }
  </script>

  <style scoped>

  </style>