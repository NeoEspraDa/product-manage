<template>
  <select name="cno3" class="custom-select">
    <option v-for="(option, index) in smallCategory"
            v-bind:key="index" v-bind:value="option.value">
      {{ option.text }}
    </option>
  </select>
</template>

<script>
export default {
  name: 'SmallCategory.vue',
  props: ['smallCategory'],
};
</script>

<style scoped>

</style>
