<template>
  <div>
    <h1>This is the reactivity page</h1>
    <div>
      {{ post }}
    </div>
    <input @input="$event => handleInput($event.target.value) ">
    <MyButton @click="editPost()">EDIT POST</MyButton>
  </div>
</template>

<script>
import MyButton from "@/components/MyButton.vue"

export default {
  props: {
    post: String
  },
  data: function () {
    return {
      textfieldValue: ""
    }
  },
  components: {
    MyButton
  },
  methods: {
    handleInput (newVal) {
      this.textfieldValue = newVal
    },
    editPost () {
      console.log("text field value =", this.textfieldValue)
      this.$emit("post-edit", this.textfieldValue)
    }
  }
}
</script>