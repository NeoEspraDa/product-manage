<template>
  <div class="accordion p-4" id="accordionExample">
    <div class="card">
      <div class="card-header" id="headingOne">
        <h2 class="mb-0">
          <button class="btn btn-link btn-block text-left"
                  type="button"
                  data-toggle="collapse"
                  data-target="#collapseOne"
                  aria-expanded="true"
                  aria-controls="collapseOne">
            상품 기본정보
          </button>
        </h2>
      </div>
      <div id="collapseOne"
           class="collapse show"
           aria-labelledby="headingOne"
           data-parent="#accordionExample">
        <div class="card-body">
          <Base />
        </div>
      </div>
    </div>
    <div class="card">
      <div class="card-header" id="headingTwo">
        <h2 class="mb-0">
          <button class="btn btn-link btn-block text-left collapsed"
                  type="button"
                  data-toggle="collapse"
                  data-target="#collapseTwo"
                  aria-expanded="false"
                  aria-controls="collapseTwo">
            상품 옵션
          </button>
        </h2>
      </div>
      <div id="collapseTwo"
           class="collapse"
           aria-labelledby="headingTwo"
           data-parent="#accordionExample">
        <div class="card-body">
          <Option />
        </div>
      </div>
    </div>
    <div class="card">
      <div class="card-header" id="headingThree">
        <h2 class="mb-0">
          <button class="btn btn-link btn-block text-left collapsed"
                  type="button"
                  data-toggle="collapse"
                  data-target="#collapseThree"
                  aria-expanded="false"
                  aria-controls="collapseThree">
            상품 정보고시
          </button>
        </h2>
      </div>
      <div id="collapseThree"
           class="collapse"
           aria-labelledby="headingThree"
           data-parent="#accordionExample">
        <div class="card-body">
          <Info />
        </div>
      </div>
    </div>
    <div class="card">
      <div class="card-header" id="headingFour">
        <h2 class="mb-0">
          <button class="btn btn-link btn-block text-left"
                  type="button"
                  data-toggle="collapse"
                  data-target="#collapseFour"
                  aria-expanded="false"
                  aria-controls="collapseFour">
            상품 기본정보 (컴포넌트 반복 테스트용)
          </button>
        </h2>
      </div>
      <div id="collapseFour"
           class="collapse"
           aria-labelledby="headingFour"
           data-parent="#accordionExample">
        <div class="card-body">
          <Base />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Base from '../components/product/Base.vue';
import Option from '../components/product/Option.vue';
import Info from '../components/product/Info.vue';

export default {
  name: 'Product',
  components: {
    Base,
    Option,
    Info,
  },
};
</script>

<style scoped>

</style>
