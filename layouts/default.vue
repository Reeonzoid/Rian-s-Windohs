<template>
  <div>
    <nuxt />
    <div class="startBar__wrapper">

      <div class="startBar__CTA" v-on:click='open = !open '>
        <span class="startBar__text">
        {{ first }}</span>
      </div>
      <startMenu v-if="open == true"></startMenu>
    </div>

  </div> 
</template>

<style>
</style>

<script>
import startMenu from "~/components/startMenu.vue"

export default {
  data () {
    return {
      first: "Start",
      open: false
    }
  },
    components: {
      startMenu
    }
}

</script>