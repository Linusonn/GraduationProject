<template>
  <div style="padding: 10px">
<!--    功能区域-->
    <div style="margin: 10px 0">
      <el-button type="primary" @click="add">新增</el-button>
      <el-button type="primary">导入</el-button>
      <el-button type="primary">导出</el-button>
    </div>
<!--    搜索区域-->
    <div style="margin: 10px 0">
      <el-input v-model="search" placeholder="Please input" style="width: 20%"/>
      <el-button type="primary" style="margin-left: 5px">查询</el-button>
    </div>

    <el-table :data="tableData" border stripe style="width: 100%">
      <el-table-column prop="id" label="ID" sortable/>
      <el-table-column prop="username" label="用户名" sortable/>
      <el-table-column prop="nickName" label="昵称" sortable/>
      <el-table-column prop="age" label="年龄" sortable/>
      <el-table-column prop="sex" label="性别" sortable/>
      <el-table-column prop="address" label="地址" sortable/>
      <el-table-column fixed="right" label="Operations" width="120">
        <template #default>
          <el-button type="text"  @click="handleEdit">Edit</el-button>
          <el-popconfirm title="Are you sure to delete this?">
            <template #reference>
              <el-button type="text" >Delete</el-button>
            </template>
          </el-popconfirm>
        </template>
      </el-table-column>
    </el-table>
    <div style="margin: 10px 0">
      <el-pagination
          :currentPage="currentPage"
          :page-size="10"
          :page-sizes="[5, 10, 20]"
          layout="total, sizes, prev, pager, next, jumper"
          :total="total"
          @size-change="handleSizeChange"
          @current-change="handleCurrentChange"
      />
      <el-dialog
          v-model="dialogVisible"
          title="Tips"
          width="30%"
      >
        <el-form :model="form" label-width="120px">
          <el-form-item label="用户名">
            <el-input v-model="form.username" style="width: 80%;"/>
          </el-form-item>
          <el-form-item label="昵称">
            <el-input v-model="form.nickName" style="width: 80%;"/>
          </el-form-item>
          <el-form-item label="年龄">
            <el-input v-model="form.age" style="width: 80%;"/>
          </el-form-item>
          <el-form-item label="性别">
            <el-radio v-model="form.sex" label="男">男</el-radio>
            <el-radio v-model="form.sex" label="女">女</el-radio>
            <el-radio v-model="form.sex" label="未知">未知</el-radio>
          </el-form-item>
          <el-form-item label="地址">
            <el-input type="textarea" v-model="form.address" style="width: 80%;"/>
          </el-form-item>

        </el-form>

        <template #footer>
      <span class="dialog-footer">
        <el-button @click="dialogVisible = false">Cancel</el-button>
        <el-button type="primary" @click="save"
        >Confirm</el-button
        >
      </span>
        </template>
      </el-dialog>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {

  },
  data() {
    return{
      search:'',
      tableData:[

      ],
      total:10,
      currentPage:1,
      dialogVisible:false,
      form:{}
    }
  },
  methods:{
    add(){
      this.dialogVisible =true
      this.form={}
    },
    save(){

    },
    handleEdit(){

    },
    handleSizeChange(){

    },
    handleCurrentChange(){

    }
  }
}
</script>
