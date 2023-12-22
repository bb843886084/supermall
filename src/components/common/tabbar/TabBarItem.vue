<template>
  <div class="tab-bar-item" @click="itemClick">
    <div>
      <slot name="item-icon"></slot>
    </div>
    <div>
      <slot name="item-text"></slot>
    </div>

    <!-- <img src="../../assets/img/logo.png" alt="">
    <div>首页</div> -->
  </div>
</template>

<script>
export default {
  name: "tabbaritem",
  props: {
    path: String,
  },
  methods: {
    itemClick() {
      this.$router.replace(this.path);
    },
  },
};
</script>




<style scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px;
  font-size: 14px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
  margin-bottom: 3px;
}
</style>