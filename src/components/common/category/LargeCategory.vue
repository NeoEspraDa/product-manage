<template>
  <select name="cno1" class="custom-select" @change="changeCNo1($event)">
    <option v-for="(option, index) in largeCategory"
            v-bind:key="index" v-bind:value="option.value">
      {{ option.text }}
    </option>
  </select>
</template>

<script>
export default {
  name: 'LargeCategory.vue',
  props: ['largeCategory'],
  methods: {
    changeCNo1(event) {
      if (event.target.value !== '') {
        this.$emit('changeCNo1', event.target.value);
      }
    },
  },
};
</script>

<style scoped>

</style>
