<template>
  <v-app>
    <SideBar @selectOption= "onSelectOption" />
    <v-main>
      <ImageGallary :isWithColor="isWithColor" />
    </v-main>
  </v-app>
   
</template>

<script setup>
  import SideBar from "./components/SideBar.vue"
  import ImageGallary from "./components/ImageGallary.vue"
  import {ref} from 'vue'

  const isWithColor = ref(true)
  const onSelectOption = (isColor) => {
    isWithColor.value = isColor
  }
</script>
