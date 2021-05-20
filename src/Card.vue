<template lang="html">
  <div @mouseover="hover = true" @mouseleave="hover = false" class="relative">
    <img :src="src" alt="" class="rounded-lg">
    <div v-if="hover" class="absolute bg-dark opacity-50 inset-0 w-full h-full rounded-lg"></div>
    <div v-if="hover" class="absolute top-0 w-full h-full flex flex-col justify-between p-3">
      <div class="flex items-center justify-between">
        <button type="button" name="button" class="flex items-center">
          <p class="font-semibold text-white"> {{ board }} </p>
          <span class="material-icons text-white">expand_more</span>
        </button>
        <button type="button" name="button" class="rounded-full py-3 px-5 text-white bg-primary font-semibold">
          Save
        </button>
      </div>
      <div class="flex items-center w-full">
        <button type="button" name="button" class="ml-auto mr-2 bg-white rounded-full w-8 h-8 flex items-center justify-center text-sm text-dark opacity-75 hover:opacity-100">
          <span class="material-icons text-base">ios_share</span>
        </button>
        <button type="button" name="button" class="bg-white rounded-full w-8 h-8 flex items-center justify-center text-dark opacity-75 hover:opacity-100">
          <span class="material-icons text-base">more_horiz</span>
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['src', 'board'],
  data() {
    return {
      hover: false
    }
  }
}
</script>

<style lang="css" scoped>
</style>
