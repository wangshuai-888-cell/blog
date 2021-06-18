<template>
  <div class="foot">
    <div class="border-bottom border-top bg-navcolor">
      <div class="d-flex py-6 jc-center">
        <div class="px-7 hand">
          <a href="https://github.com/wangshuai-888-cell" target="_blank" class="text-grey-1">GITHUB</a>
        </div>
        <div class="px-7 hand">
          <a
            href="https://www.zhihu.com/people/liu-fang-tao-hua-an-30"
            target="_blank"
            class="text-grey-1"
          >知乎</a>
        </div>
        <div class="px-7 hand">
          <a
            href="https://weibo.com/6380283658/profile?rightmod=1&wvr=6&mod=personinfo&is_all=1"
            target="_blank"
            class="text-grey-1"
          >微博</a>
        </div>
      </div>
    </div>

  </div>
</template>

<script>

export default {
  data() {
    return {
      model: [],
      intTime: null
    };
  },
  created() {
  },
  methods: {
    async fetchArticles() {
      const res = await this.$http.get("articles/recent");
      this.model = res.data;
    }
  },
  mounted() {
    this.fetchArticles();
  }
};
</script>

<style lang="scss" scoped>
.foot {
  width: 100%;
  bottom: 0;
  left: 0;
}
</style>
