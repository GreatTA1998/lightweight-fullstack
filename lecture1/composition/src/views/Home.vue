<template>
  <div>
    <template v-for="post in facebookPosts">
      <MyCard :title="post" :key="post">
        <!-- <v-btn
        text
        color="deep-purple accent-4"
      >
        Learn More
      </v-btn> -->
      <!-- <v-btn
        text
        color="deep-purple accent-4"
      >
        Learn More
      </v-btn> -->
        <MyButton @click="myFunc1()"></MyButton>
        <MyButton @click="myFunc2()"></MyButton>


      </MyCard>
    </template>
  </div>
</template>

<script>
import MyCard from "@/components/MyCard.vue"
import MyButton from "@/components/MyButton.vue"

export default {
  components: {
    MyCard,
    MyButton
  },
  data: function () {
    return {
      facebookPosts: ["firstPost", "politics", "sports"]
    }
  },
  methods: {
    myFunc1 () {
      alert("THIS IS THE FIRST")
    },
    myFunc2 () {
      alert("THIS IS THE SECOND")
    }
  }
}
</script>