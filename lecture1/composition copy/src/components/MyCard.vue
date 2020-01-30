<template>
  <div>
      <template>
  <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-card-text>
      <div>Word of the Day</div>
      <p class="display-1 text--primary">
        {{ title }}
      </p>
      <p>adjective</p>
      <div class="text--primary">
        well meaning and kindly.<br>
        "a benevolent smile"
      </div>
    </v-card-text>
    <v-card-actions>
      <slot>
     
      </slot>
    </v-card-actions>
  </v-card>
</template>


<!--     
    <h1>{{ title }}</h1>
    <MyButton></MyButton>
    <MyButton></MyButton> -->
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