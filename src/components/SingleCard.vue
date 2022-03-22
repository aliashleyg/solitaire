<template>
  <div class="parent">
    <div class="cardPileForFlipping">
      <ul>
        <li v-for="card in cardStack" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
    </div>
    <div class="cardRowGrid">
      <ul>
        <li v-for="card in rowOfSeven" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
      <ul>
        <li v-for="card in rowOfSix" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
      <ul>
        <li v-for="card in rowOfFive" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
      <ul>
        <li v-for="card in rowOfFour" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
      <ul>
        <li v-for="card in rowOfThree" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
      <ul>
        <li v-for="card in rowOfTwo" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
      <ul>
        <li v-for="card in rowOfOne" :key="card.image">
          <img :src="card.image" class="single-card">
        </li>
      </ul>
    </div>
  </div>

</template>

<script>
import aceOfClubs from "../assets/cards/c-1.png";
import twoOfClubs from "../assets/cards/c-2.png";
import threeOfClubs from "../assets/cards/c-3.png";
import fourOfClubs from "../assets/cards/c-4.png";
import fiveOfClubs from "../assets/cards/c-5.png";
import sixOfClubs from "../assets/cards/c-6.png";
import sevenOfClubs from "../assets/cards/c-7.png";
import eightOfClubs from "../assets/cards/c-8.png";
import nineOfClubs from "../assets/cards/c-9.png";
import tenOfClubs from "../assets/cards/c-10.png";
import jackOfClubs from "../assets/cards/c-11.png";
import queenOfClubs from "../assets/cards/c-12.png";
import kingOfClubs from "../assets/cards/c-13.png";

import aceOfDiamonds from "../assets/cards/d-1.png";
import twoOfDiamonds from "../assets/cards/d-2.png";
import threeOfDiamonds from "../assets/cards/d-3.png";
import fourOfDiamonds from "../assets/cards/d-4.png";
import fiveOfDiamonds from "../assets/cards/d-5.png";
import sixOfDiamonds from "../assets/cards/d-6.png";
import sevenOfDiamonds from "../assets/cards/d-7.png";
import eightOfDiamonds from "../assets/cards/d-8.png";
import nineOfDiamonds from "../assets/cards/d-9.png";
import tenOfDiamonds from "../assets/cards/d-10.png";
import jackOfDiamonds from "../assets/cards/d-11.png";
import queenOfDiamonds from "../assets/cards/d-12.png";
import kingOfDiamonds from "../assets/cards/d-13.png";

import aceOfHearts from "../assets/cards/h-1.png";
import twoOfHearts from "../assets/cards/h-2.png";
import threeOfHearts from "../assets/cards/h-3.png";
import fourOfHearts from "../assets/cards/h-4.png";
import fiveOfHearts from "../assets/cards/h-5.png";
import sixOfHearts from "../assets/cards/h-6.png";
import sevenOfHearts from "../assets/cards/h-7.png";
import eightOfHearts from "../assets/cards/h-8.png";
import nineOfHearts from "../assets/cards/h-9.png";
import tenOfHearts from "../assets/cards/h-10.png";
import jackOfHearts from "../assets/cards/h-11.png";
import queenOfHearts from "../assets/cards/h-12.png";
import kingOfHearts from "../assets/cards/h-13.png";

import aceOfSpades from "../assets/cards/s-1.png";
import twoOfSpades from "../assets/cards/s-2.png";
import threeOfSpades from "../assets/cards/s-3.png";
import fourOfSpades from "../assets/cards/s-4.png";
import fiveOfSpades from "../assets/cards/s-5.png";
import sixOfSpades from "../assets/cards/s-6.png";
import sevenOfSpades from "../assets/cards/s-7.png";
import eightOfSpades from "../assets/cards/s-8.png";
import nineOfSpades from "../assets/cards/s-9.png";
import tenOfSpades from "../assets/cards/s-10.png";
import jackOfSpades from "../assets/cards/s-11.png";
import queenOfSpades from "../assets/cards/s-12.png";
import kingOfSpades from "../assets/cards/s-13.png";

import cardBack from "../assets/cards/back.png";

export default {
  data() {
    return {
      shuffledCards: [],
      rowOfSeven: [],
      rowOfSix: [],
      rowOfFive: [],
      rowOfFour: [],
      rowOfThree: [],
      rowOfTwo: [],
      rowOfOne: [],
      cardStack: [],
      showCardFace: false,
      cards: [
        {
          id: 1,
          randomCardId: Number,
          cardValue: "clubs1",
          image: aceOfClubs,
          numValue: 1,
        },
        {
          id: 2,
          randomCardId: Number,
          cardValue: "clubs2",
          image: twoOfClubs,
          numValue: 2
        },
        {
          id: 3,
          randomCardId: Number,
          cardValue: "clubs3",
          image: threeOfClubs,
          numValue: 3
        },
        {
          id: 4,
          randomCardId: Number,
          cardValue: "clubs4",
          image: fourOfClubs,
          numValue: 4
        },
        {
          id: 5,
          randomCardId: Number,
          cardValue: "clubs5",
          image: fiveOfClubs,
          numValue: 5
        },
        {
          id:6,
          cardValue: "clubs6",
          image: sixOfClubs,
          numValue: 6

        },
        {
          id:7,
          cardValue: "clubs7",
          image: sevenOfClubs,
          numValue: 7
        },
        {
          id:8,
          cardValue: "clubs8",
          image: eightOfClubs,
          numValue: 8
        },
        {
          id:9,
          cardValue: "clubs9",
          image: nineOfClubs,
          numValue: 9
        },
        {
          id:10,
          cardValue: "clubs10",
          image: tenOfClubs,
          numValue: 11
        },
        {
          id:11,
          cardValue: "clubs11",
          image: jackOfClubs,
          numValue: 11
        },
        {
          id:12,
          cardValue: "clubs12",
          image: queenOfClubs,
          numValue: 12
        },
        {
          id:13,
          cardValue: "clubs13",
          image: kingOfClubs,
          numValue: 13
        },
        {
          id:14,
          cardValue: "diamonds1",
          image: aceOfDiamonds,
          numValue: 1
        },
        {
          id:15,
          cardValue: "diamonds2",
          image: twoOfDiamonds,
          numValue: 2
        },
        {
          id:16,
          cardValue: "diamonds3",
          image: threeOfDiamonds,
          numValue: 3
        },
        {
          id:17,
          cardValue: "diamonds4",
          image: fourOfDiamonds,
          numValue: 4
        },
        {
          id:18,
          cardValue: "diamonds5",
          image: fiveOfDiamonds,
          numValue: 5
        },
        {
          id:19,
          cardValue: "diamonds6",
          image: sixOfDiamonds,
          numValue: 6

        },
        {
          id:20,
          cardValue: "diamonds7",
          image: sevenOfDiamonds,
          numValue: 7
        },
        {
          id:21,
          cardValue: "diamonds8",
          image: eightOfDiamonds,
          numValue: 8
        },
        {
          id:22,
          cardValue: "diamonds9",
          image: nineOfDiamonds,
          numValue: 9
        },
        {
          id:23,
          cardValue: "diamonds10",
          image: tenOfDiamonds,
          numValue: 11
        },
        {
          id:24,
          cardValue: "diamonds11",
          image: jackOfDiamonds,
          numValue: 11
        },
        {
          id:25,
          cardValue: "diamonds12",
          image: queenOfDiamonds,
          numValue: 12
        },
        {
          id:26,
          cardValue: "diamonds13",
          image: kingOfDiamonds,
          numValue: 13
        },
        {
          id:27,
          cardValue: "hearts1",
          image: aceOfHearts,
          numValue: 1
        },
        {
          id:28,
          cardValue: "hearts2",
          image: twoOfHearts,
          numValue: 2
        },
        {
          id:29,
          cardValue: "hearts3",
          image: threeOfHearts,
          numValue: 3
        },
        {
          id:30,
          cardValue: "hearts4",
          image: fourOfHearts,
          numValue: 4
        },
        {
          id:31,
          cardValue: "hearts5",
          image: fiveOfHearts,
          numValue: 5
        },
        {
          id:32,
          cardValue: "hearts6",
          image: sixOfHearts,
          numValue: 6

        },
        {
          id:33,
          cardValue: "hearts7",
          image: sevenOfHearts,
          numValue: 7
        },
        {
          id:34,
          cardValue: "hearts8",
          image: eightOfHearts,
          numValue: 8
        },
        {
          id:35,
          cardValue: "hearts9",
          image: nineOfHearts,
          numValue: 9
        },
        {
          id:36,
          cardValue: "hearts10",
          image: tenOfHearts,
          numValue: 11
        },
        {
          id:37,
          cardValue: "hearts11",
          image: jackOfHearts,
          numValue: 11
        },
        {
          id:38,
          cardValue: "hearts12",
          image: queenOfHearts,
          numValue: 12
        },
        {
          id:39,
          cardValue: "hearts13",
          image: kingOfHearts,
          numValue: 13
        },
        {
          id:40,
          cardValue: "spades1",
          image: aceOfSpades,
          numValue: 1
        },
        {
          id:41,
          cardValue: "spades2",
          image: twoOfSpades,
          numValue: 2
        },
        {
          id:42,
          cardValue: "spades3",
          image: threeOfSpades,
          numValue: 3
        },
        {
          id:43,
          cardValue: "spades4",
          image: fourOfSpades,
          numValue: 4
        },
        {
          id:44,
          cardValue: "spades5",
          image: fiveOfSpades,
          numValue: 5
        },
        {
          id:45,
          cardValue: "spades6",
          image: sixOfSpades,
          numValue: 6

        },
        {
          id:46,
          cardValue: "spades7",
          image: sevenOfSpades,
          numValue: 7
        },
        {
          id:47,
          cardValue: "spades8",
          image: eightOfSpades,
          numValue: 8
        },
        {
          id:48,
          cardValue: "spades9",
          image: nineOfSpades,
          numValue: 9
        },
        {
          id:49,
          cardValue: "spades10",
          image: tenOfSpades,
          numValue: 11
        },
        {
          id:50,
          cardValue: "spades11",
          image: jackOfSpades,
          numValue: 11
        },
        {
          id:51,
          cardValue: "spades12",
          image: queenOfSpades,
          numValue: 12
        },
        {
          id:52,
          cardValue: "spades13",
          image: kingOfSpades,
          numValue: 13
        },
      ],
      backOfCard: {
        id:-1,
        cardValue: "back",
        image: cardBack,
        numValue: 0
      }
    }
  },
  methods: {
    shuffleCards() {
      this.shuffledCards = this.cards; //array
      let numberOfCards = this.shuffledCards.length;  //m
      while (numberOfCards) {
        let randomNumber = Math.floor(Math.random() * numberOfCards--); //i
        let shallowArray = this.shuffledCards[numberOfCards];  //t
        this.shuffledCards[numberOfCards] = this.shuffledCards[randomNumber];
        this.shuffledCards[randomNumber] = shallowArray;
      }
      return this.shuffledCards;
    },
    assignCardsToRows() {
      while (this.shuffledCards.length > 0) {
        this.rowOfSeven = this.shuffledCards.splice(0,7);
        this.rowOfSix = this.shuffledCards.splice(0, 6);
        this.rowOfFive = this.shuffledCards.splice(0, 5);
        this.rowOfFour = this.shuffledCards.splice(0, 4);
        this.rowOfThree = this.shuffledCards.splice(0, 3);
        this.rowOfTwo = this.shuffledCards.splice(0,2);
        this.rowOfOne = this.shuffledCards.splice(0,1);
        this.cardStack = this.shuffledCards.splice(0);
      }
    },
    showLastCardOfRow(cardRow) {
      let i = 0;
      while (i <= cardRow.length - 1) {
        if (i < cardRow.length - 1) {
          cardRow[i].image = this.backOfCard.image;
        }
        i++;
      }
    }
  },
  created() {
    this.shuffleCards();
    this.assignCardsToRows();
    this.showLastCardOfRow(this.rowOfSeven);
    this.showLastCardOfRow(this.rowOfSix);
    this.showLastCardOfRow(this.rowOfFive);
    this.showLastCardOfRow(this.rowOfFour);
    this.showLastCardOfRow(this.rowOfThree);
    this.showLastCardOfRow(this.rowOfTwo);
    this.showLastCardOfRow(this.rowOfOne);
    this.showLastCardOfRow(this.cardStack);
  }
}
</script>

<style>

.cardRowGrid {
  display: grid;
  grid-template-columns: repeat(7, 180px);
  margin: 5rem;
  max-width: 100%;
  grid-column-gap: 1rem;
}

.single-card {
width: 180px;
}

li {
  list-style: none;
  display: block;
  margin-top: -240px;

}

li:first-child {
  margin-top: 0px;
}

.cardPileForFlipping {
  display: inline;
}

.cardPileForFlipping li {
  display: inline;
  margin-right: -175px;
}
</style>



