<script setup lang="ts">
import HeaderButtonComponent from '../lib/HeaderButtonComponent.vue'
import VideoWithTextComponent from '../lib/VideoWithTextComponent.vue'
import FooterComponent from '../lib/FooterComponent.vue'
import ButtonComponent from '../lib/ButtonComponent.vue'
import VerticalTimelineComponent from '../lib/VerticalTimelineComponent.vue'
import HorizontalTimelineComponent from '../lib/HorizontalTimelineComponent.vue'

function test() {
  console.log("TEST")
}

const timelines = [
  {
    startEndDate: "June 2018 - June 2025",
    organization: "REWE International AG",
    position: "iOS Software Engineer & Backend Developer",
    description: "Responsible for the development of eCommerce iOS white-label applications for Billa Austria and Czech Republic, utilizing cutting-edge iOS technologies such as SwiftUI, UIKit, Async/Await, and TCA. Co-developed the gateway using Kotlin, Spring Boot, Spring Security, and Spring Data, while also designing API drafts to provide efficient interfaces for Android and iOS clients."
  },
  {
    startEndDate: "June 2019 - June 2021",
    organization: "Marzek",
    position: "iOS Software Engineer & Backend Developer",
    description: "Responsible for the development of eCommerce iOS white-label applications for Billa Austria and Czech Republic, utilizing cutting-edge iOS technologies such as SwiftUI, UIKit, Async/Await, and TCA. Co-developed the gateway using Kotlin, Spring Boot, Spring Security, and Spring Data, while also designing API drafts to provide efficient interfaces for Android and iOS clients."
  },
  {
    startEndDate: "June 2019 - June 2021",
    organization: "Marzek",
    position: "iOS Software Engineer & Backend Developer",
    description: "Responsible for the development of eCommerce iOS white-label applications for Billa Austria and Czech Republic, utilizing cutting-edge iOS technologies such as SwiftUI, UIKit, Async/Await, and TCA. Co-developed the gateway using Kotlin, Spring Boot, Spring Security, and Spring Data, while also designing API drafts to provide efficient interfaces for Android and iOS clients."
  }
]

</script>

<template>
  <div class="bg-white">
    <!-- <VideoWithTextComponent videoName="Test Button" v-bind:headerTitleTexts="['HEY,', 'THIS', 'IS', 'EBU']"
      v-bind:headerBodyTexts="['Software Engineer', '|', 'Unversity Lecturer', '|', 'Gym Enthusiast']"
      v-bind:headerButtonText="'Get in Touch'" :onButtonClick="test" />
    <ButtonComponent text="Test" link="mailto:ebucelik1@hotmail.com" />
    <ButtonComponent text="Test leer" link="" class="text-white" />
    <ButtonComponent text="Test Null" v-on:click="test" />
    <FooterComponent class="mx-auto px-5 lg:px-10" /> -->

    <FooterComponent class="mx-auto px-5 lg:px-10" />
    <VerticalTimelineComponent v-bind:timelines="timelines" />
    <HorizontalTimelineComponent v-bind:timelines="timelines" />
  </div>
</template>