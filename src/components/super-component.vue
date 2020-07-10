<template>
  <!-- <div> -->
  <div class="h-42 w-64 shadow-xl m-auto mt-12 rounded-md p-2">
    <h3 class>Super Component Info</h3>
    <div class="flex flex-col mt-5">
      <label class="text-xs" for="box">Random Label</label>
      <input id="box" type="text" />
    </div>
    <button
      v-bind="filtered"
      class="border-black rounded-lg p-2 border mt-5 focus:outline-none text-green-300"
    >Press Me</button>
  </div>
  <!-- </div> -->
</template>

<script>
export default {
  inheritAttrs: false,
  computed: {
    filtered() {
      const newAttrs = { ...this.$attrs };
      delete newAttrs.class;
      return newAttrs;
    }
  }
};
</script>

<style scoped></style>
