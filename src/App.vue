<script setup lang="ts">
import HeaderButtonComponent from '../lib/HeaderButtonComponent.vue'
import VideoWithTextComponent from '../lib/VideoWithTextComponent.vue'
import FooterComponent from '../lib/FooterComponent.vue'
import ButtonComponent from '../lib/ButtonComponent.vue'

function test() {
  console.log("TEST")
}

</script>

<template>
  <div>
    <VideoWithTextComponent videoName="Test Button" :onButtonClick="test" />
    <ButtonComponent text="Test" link="mailto:ebucelik1@hotmail.com" />
    <ButtonComponent text="Test leer" link="" />
    <ButtonComponent text="Test Null" v-on:click="test" />
    <FooterComponent />
  </div>
</template>

<style>
html {
  background-color: gray;
}
</style>