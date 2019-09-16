<template>
  <el-table
    :data="tableData"
    style="width: 100%"
    border
  >
    <el-table-column
      prop="concurrency"
      label="并发数"
    >
    </el-table-column>
    <el-table-column
      prop="loop"
      label="循环迭代"
    >
    </el-table-column>
    <el-table-column
      prop="type"
      label="交易类型"
    >
    </el-table-column>
    <el-table-column
      prop="ip"
      label="IP地址"
    >
    </el-table-column>
    <el-table-column
      prop="serial"
      label="流水号"
    >
    </el-table-column>
    <el-table-column
      prop="delete"
      label="是否删除"
    >
    </el-table-column>
    <el-table-column
      prop="operation"
      label="操作"
    >
      <template>
        <el-button type="text" size="small">删除</el-button>
        <el-button type="text" size="small">启动</el-button>
        <el-button type="text" size="small" @click="open">编辑</el-button>
      </template>
    </el-table-column>
    <el-table-column
      prop="remake"
      label="备注"
    >
    </el-table-column>
  </el-table>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
          tableData: [{
            concurrency: 1,
            loop: 1,
            type: '1900/1/2',
            ip: '2.2.2.2',
            serial: 222,
            delete: '0:00',
            remake:'god yu'
          }]
        }
  },
  methods: {
    open() {
      this.$alert('高宇是崴子', '崴子高宇', {
        confirmButtonText: '确定',
        callback: action => {
          this.$message({
            type: 'info',
            message: `${action} 吔屎啦你`,
          });
        }
      });
    }
  }
}
</script>
