<template>
  <div>
    <Row class="header">
      <Col :xs="12" :sm="12" :md="8" :lg="8">
        <h2>{{ mainTitle }}</h2>
      </Col>
      <template v-for="(item, index) in headerList">
        <Col :key="index">
          <h3>{{ item.title }}</h3>
        </Col>
      </template>
    </Row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      mainTitle: "毛孩鮮食救星",
      headerList: [
        {
          title: "近期活動",
          path: "/activity",
        },
        {
          title: "毛孩寫真",
          path: "/activity",
        },
        {
          title: "領養資訊",
          path: "/activity",
        },
      ],
    }
  },
  methods: {
    toPage (path) {
      this.$router.push({
        path: path,
      });
    },
  },
}
</script>
<style lang="scss" scoped>
.header {
  background-color: #fff;
  height: 64px;
  box-shadow: 1px 2px 5px #eee;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
</style>
