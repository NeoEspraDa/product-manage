<template>
  <div>
    <div class="form-group input-group">
      <div class="col-sm-2">
        상품명
      </div>
      <div class="col-sm-10">
        <input type="text" class="form-control" placeholder="상품명을 입력해주세요">
      </div>
    </div>
    <Category />
  </div>
</template>

<script>
import Category from '../common/category/Category.vue';

export default {
  name: 'Base.vue',
  components: {
    Category,
  },
};
</script>

<style scoped>

</style>
