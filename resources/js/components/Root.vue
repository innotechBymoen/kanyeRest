<template>
  <div id='grid-container'>
    <Button />
    <Quote />
  </div>
</template>

<script>
import Button from "./Button.vue";
import Quote from "./Quote.vue";

export default {
  name: "Root",
  components: {
    Button,
    Quote
  }
};
</script>

<style>
    body {
        font-family: Nunito
    }

    #grid-container {
        min-height: 50vh;
        display: grid;
        grid-template-rows: 1fr 1fr;
        justify-items: center;
        align-items: center;
    }
</style>
