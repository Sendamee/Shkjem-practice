<template>
  <div class="faq-pc">
    <!-- 文本区外部容器 -->
    <div class="main">
      <!-- 折叠面板 -->
      <el-collapse v-for="(item, index) in collapsItemData" :key="index">
        <el-collapse-item>
          <template slot="title">
            <i class="el-icon-s-comment" style="color: #ff9857"></i>
            <span class="title">{{ item.title }}</span>
          </template>
          <div>{{ item.p1 }}</div>
          <br />
          <div>{{ item.p2 }}</div>
          <br />
          <div>{{ item.p3 }}</div>
        </el-collapse-item>
      </el-collapse>
    </div>
  </div>
</template>

<script>
import faq from "@/faq-content";
export default {
  name: "Faq",
  data() {
    return {
      collapsItemData: faq(),
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
.faq-pc {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  margin-bottom: 200px;
  .main {
    width: 750px;
    font-size: 12px;
    color: #000000;
    border-top: 1px solid #ebeef5;
    .el-collapse {
      border-top: none;
       .el-collapse-item__header{
        border-bottom: none;
      }
      .el-icon-s-comment {
        font-size: 1.4em;
        margin-right: 10px;
      }
      .title {
        font-size: 1.4em;
        font-family: Helvetica;
        font-style: Oblique;
        font-weight: bold;
      }
    }
  }
}
</style>