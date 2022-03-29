<template>
    <div style="height: 50px; line-height: 50px; border-bottom: 1px solid #ccc; display: flex">
      <div style="width: 200px; padding-left:30px; font-weight: bold; color: dodgerblue">后台管理</div>
      <div style="flex:1"></div>
      <div style="width: 100px">
        <el-dropdown>
          <el-button type="primary" >
            Dropdown List<el-icon class="el-icon--right"><arrow-down /></el-icon>
          </el-button>
          <template #dropdown>
            <el-dropdown-menu>
              <el-dropdown-item>Action 1</el-dropdown-item>
              <el-dropdown-item>Action 2</el-dropdown-item>
              <el-dropdown-item>Action 3</el-dropdown-item>
              <el-dropdown-item>Action 4</el-dropdown-item>
              <el-dropdown-item>Action 5</el-dropdown-item>
            </el-dropdown-menu>
          </template>
        </el-dropdown>
      </div>
    </div>
</template>

<script>


export default ({
    name: "Header"
})
</script>

<style scoped>

</style>