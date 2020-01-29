<template>
  <button @click="$emit('click')" color="purple">button</button>
</template>

<script>
export default {
  name: "my-button",
  methods: {
    myFunc: function () {
      alert("Hello")
    },
  }
}
</script>