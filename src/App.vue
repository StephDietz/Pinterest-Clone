<template>
  <div class="">
    <TopNav />
    <div class="px-20 w-full flex flex-wrap">
      <div v-for="(arr, index) in subArrays" :key="index" class="w-1/5">
        <div v-for="(card, i) in arr" :key="i" class="w-full">
          <div class="w-full p-2">
            <Card :src="`${card.src}`" :board="`${card.recommended}`" class="w-full h-full"/>
            <div class="text-sm leading-tight pt-2">
              <p class="font-bold"> {{ card.title }} </p>
              <p> {{ card.user }} </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopNav from './TopNav.vue';
import Card from './Card.vue';

export default {
  name: 'App',
  components: {
    TopNav,
    Card
  },
  computed: {
    subArrays() {
      var length = Math.ceil(this.cards.length / 5);

      const result = new Array(length)
        .fill()
        .map((i) => {
          console.log(i)
          return this.cards.splice(0, length)
        })

        return result
    }
  },
  data() {
    return {
      cards: [
        {
          src: '1.jpg',
          title: 'Title 1',
          user: 'User 1',
          recommended: 'Travel'
        },
        {
          src: '2.jpg',
          title: 'Title 2',
          user: 'User 2',
          recommended: 'Travel'
        },
        {
          src: '3.jpg',
          title: 'Title 3',
          user: 'User 3',
          recommended: 'Travel'
        },
        {
          src: '4.jpg',
          title: 'Title 4',
          user: 'User 4',
          recommended: 'Travel'
        },
        {
          src: '5.jpg',
          title: 'Title 5',
          user: 'User 5',
          recommended: 'Travel'
        },
        {
          src: '6.jpg',
          title: 'Title 6',
          user: 'User 6',
          recommended: 'Travel'
        },
        {
          src: '7.jpg',
          title: 'Title 7',
          user: 'User 7',
          recommended: 'Travel'
        },
        {
          src: '8.jpg',
          title: 'Title 8',
          user: 'User 8',
          recommended: 'Travel'
        },
        {
          src: '9.jpg',
          title: 'Title 9',
          user: 'User 9',
          recommended: 'Travel'
        },
        {
          src: '10.jpg',
          title: 'Title 10',
          user: 'User 10',
          recommended: 'Travel'
        },
        {
          src: '11.jpg',
          title: 'Title 11',
          user: 'User 11',
          recommended: 'Travel'
        },
        {
          src: '12.jpg',
          title: 'Title 12',
          user: 'User 12',
          recommended: 'Travel'
        },
        {
          src: '13.jpg',
          title: 'Title 13',
          user: 'User 13',
          recommended: 'Travel'
        },
        {
          src: '14.jpg',
          title: 'Title 14',
          user: 'User 14',
          recommended: 'Travel'
        },
        {
          src: '15.jpg',
          title: 'Title 15',
          user: 'User 15',
          recommended: 'Travel'
        },
        {
          src: '16.jpg',
          title: 'Title 16',
          user: 'User 16',
          recommended: 'Travel'
        },
        {
          src: '17.jpg',
          title: 'Title 17',
          user: 'User 17',
          recommended: 'Travel'
        },
        {
          src: '18.jpg',
          title: 'Title 18',
          user: 'User 18',
          recommended: 'Travel'
        },
        {
          src: '19.jpg',
          title: 'Title 19',
          user: 'User 19',
          recommended: 'Travel'
        },
        {
          src: '20.jpg',
          title: 'Title 20',
          user: 'User 20',
          recommended: 'Travel'
        },
        {
          src: '21.jpg',
          title: 'Title 21',
          user: 'User 21',
          recommended: 'Travel'
        },
        {
          src: '22.jpg',
          title: 'Title 22',
          user: 'User 22',
          recommended: 'Travel'
        },
        {
          src: '13.jpg',
          title: 'Title 13',
          user: 'User 13',
          recommended: 'Travel'
        },
        {
          src: '14.jpg',
          title: 'Title 14',
          user: 'User 14',
          recommended: 'Travel'
        },
        {
          src: '15.jpg',
          title: 'Title 15',
          user: 'User 15',
          recommended: 'Travel'
        },
      ]
    }
  }
}
</script>

<style src="./assets/tailwind.css" />
