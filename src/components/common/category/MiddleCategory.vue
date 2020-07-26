<template>
  <select name="cno2" class="custom-select" @change="changeCNo2($event)">
    <option v-for="(option, index) in middleCategory"
            v-bind:key="index" v-bind:value="option.value">
      {{ option.text }}
    </option>
  </select>
</template>

<script>
export default {
  name: 'MiddleCategory.vue',
  props: ['middleCategory'],
  methods: {
    changeCNo2(event) {
      this.$emit('changeCNo2', event.target.value);
    },
  },
};
</script>

<style scoped>

</style>
