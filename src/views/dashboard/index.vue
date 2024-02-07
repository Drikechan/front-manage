<template>
  <div class="dashboard-container">
    <div class="dashboard-content">
      <el-form :model="formModel" label-width="80px">
        <el-form-item label="自定义：">
          <el-input v-model="value" style="width: 200px" />
        </el-form-item>
      </el-form>
      <el-button type="primary" @click="importData">导入</el-button>
      <el-table
        :data="tableData"
        style="width: 100%"
      >
        <el-table-column
          prop="date"
          label="日期"
          width="180"
        />
        <el-table-column
          prop="name"
          label="姓名"
          width="180"
        />
        <el-table-column
          prop="address"
          label="地址"
        />
      </el-table>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Dashboard',
  data() {
    return {
      formModel: {},
      value: '',
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    }
  },
  computed: {
  },
  created() {

  },
  methods: {
    importData() {

    }
  }
}
</script>
<style scoped lang="scss">
.dashboard-container {
  min-height: calc(100vh - 84px);
  padding: 20px;
  background: #f0f2f5;
  .dashboard-content {
    height: calc(100vh - 124px);
    background: #fff;
    padding: 20px;
  }
}
</style>
