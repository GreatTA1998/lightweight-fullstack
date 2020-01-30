<template>
  <div>
    <h1>REACTIVITY PARENT</h1>
    <template v-for="(post, i) in myPosts">
      <div :key="post">
        <h1>{{ i }}</h1>
        <ReactivityChild 
          @post-edit="(newValue) => editPost(newValue, i)"
          :post="post"></ReactivityChild>
      </div>
    </template>
  </div>
</template>

<script>
import ReactivityChild from "@/components/ReactivityChild"

export default {
  components: {
    ReactivityChild
  },
  data: function () {
    return { 
      myPosts: ["Abraham Lincoln", "Einstein", "Feynman"]
    }
  },
  methods: {
    editPost (newValue, i) {
      console.log("newValue =", newValue)
      this.$set(this.myPosts, i, newValue)
    }
  }
}
</script>