<template>
  <div>
    <div>
      {{ post }}
    </div>
    <MyButton>EDIT POST</MyButton>
  </div>
</template>

<script>
import MyButton from "@/components/MyButton.vue"

export default {
  props: {
    title: String
  },
  components: {
    MyButton
  }
}
</script>