<template>
  <div class="hot">
    <p>热门文章</p>
    <div>
      <router-link :to="'/details/' + item.id" v-for="item in data" :key="item.id">{{ item.title }}</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "HotArticle",
  props: {
    data: {
      type: Array,
      required: true
    }
  }
};
</script>

<style scoped>
.hot {
  border-top: 1px solid #ececec;
  padding-bottom: 15px;
}
p {
  color: gray;
  font-weight: bold;
}
a {
  display: block;
  color: #bfbfbf;
  font-size: 14px;
  text-decoration: none;
  margin: 0 8px 0 0;
  margin-bottom: 6px;
  cursor: pointer;
}
a:hover {
  color: #0085a1;
}
</style>
