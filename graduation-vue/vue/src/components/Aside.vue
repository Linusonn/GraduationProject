<template>
  <div>
    <el-menu
        style="width: 200px; min-height: calc(100vh - 50px)"
        default-active="2"
        class="el-menu-vertical-demo"
        :default-openeds='["1"]'
    >
      <el-sub-menu index="1">
        <template #title>系统管理</template>
        <el-menu-item index="user">用户管理</el-menu-item>
      </el-sub-menu>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: "Aside"
}
</script>

<style scoped>

</style>