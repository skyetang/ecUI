<template>
    <div>
      <div style="height: 200px;">
        <el-table
          :data="tableData"
          stripe
          class="ec-table">
          <el-table-column
            prop="date"
            label="日期"
            min-width="10">
          </el-table-column>
          <el-table-column
            prop="name"
            label="姓名"
            min-width="30">
            <template scope="scope">
              <a href="javascript:;">{{ scope.row.address }}</a>
            </template>
          </el-table-column>
          <el-table-column
            prop="address"
            label="地址"
            min-width="50">
          </el-table-column>
        </el-table>
      </div>
      <br>
      <el-table
        :data="tableData"
        border
        class="ec-table-page">
        <el-table-column
          prop="date"
          label="日期"
          min-width="10">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          min-width="30">
          <template scope="scope">
            <a href="javascript:;">{{ scope.row.address }}</a>
          </template>
        </el-table-column>
        <el-table-column
          prop="address"
          label="地址"
          min-width="50">
        </el-table-column>
      </el-table>
      <br>
      <el-table
        :data="tableData"
        border
        class="ec-table-page">
        <el-table-column
          prop="date"
          label="日期"
          min-width="10">
        </el-table-column>
        <el-table-column
          prop="name"
          label="姓名"
          min-width="30">
          <template scope="scope">
            <div class="table-item-wrap">
              <p>201707070001</p>
              <p>{{ scope.row.address }}</p>
              <p> <el-input></el-input></p>
              <p> <el-input></el-input></p>
            </div>
          </template>
        </el-table-column>
        <el-table-column
          prop="address"
          label="地址"
          min-width="50">
        </el-table-column>
      </el-table>
    </div>
</template>

<script>
  export default {
    data() {
      return {
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
      };
    }
  };
</script>

