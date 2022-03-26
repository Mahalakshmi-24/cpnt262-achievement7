<template>
  <main>
   <TheHeader />

    <div class="flex flex-wrap justify-center text-align: center mt-8">
      <the-base-card v-for="card in cards" :key="card.id">
       
        <the-card-title>{{ card.title }}</the-card-title>
         <the-card-image :url="card.image" />
        <the-card-offer>{{card.offer}}</the-card-offer>
        <the-card-text>{{card.text}}</the-card-text>
        <the-card-price> {{card.price}}</the-card-price>
        <the-button> ADD TO CART</the-button>
      </the-base-card>
    </div>

  <TheFooter />
  </main>
</template>

<script setup>

import TheHeader from "./components/utilities/TheHeader.vue";
import TheBaseCard from "./components/cardlayout/TheBaseCard.vue";
import TheCardTitle from "./components/cardlayout/TheCardTitle.vue";
import TheCardImage from "./components/cardlayout/TheCardImage.vue";
import TheButton from "./components/utilities/TheButton.vue";
import TheFooter from "./components/utilities/TheFooter.vue";
import TheCardOffer from "./components/cardlayout/TheCardIOffer.vue";
import TheCardPrice from "./components/cardlayout/TheCardPrice.vue";
import TheCardText from "./components/cardlayout/TheCardText.vue";





// first card
const cards = [
  {
    title: "Candles",
    image: require('./assets/images/candles.jpg'),
    text :"Text relates to the content" ,
    offer: "BUY 3 GET 1 FREE ",
    price: "$10 OFF",
   
  },
  // second card
  {
    title: "Fragrance refill",
    image: require('./assets/images/wallflower.webp'),
    offer : "BUY 2 GET 1 FREE ",
    text :"Text relates to the content" ,
    price: "5/$25",
   
   
  },
  // third card
  {
    title: "Bodycare",
    image: require('./assets/images/bodycare.jpg'),
    offer: "BUY 3 GET 10% OFFER",
    text :"Text relates to the content" ,
    price: "Starts From $15",
   
    
  },

  
];
</script>