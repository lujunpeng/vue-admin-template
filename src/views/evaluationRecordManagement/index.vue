<!--
 * @Date: 2020-10-29 16:48:05
 * @LastEditors: lujunpeng
 * @LastEditTime: 2020-10-29 17:37:53
 * @FilePath: /bus_fe_pcweb/Users/lujunpeng/Documents/Code/qbzc/vue-admin-template/src/views/evaluationRecordManagement/index.vue
-->
<template>
  <div class="index">
    <el-table
      :data="tableData"
      stripe
      border
      style="width: 100%"
    >
      <el-table-column
        prop="name"
        label="评测编号"
        width="180"
      />
      <el-table-column
        prop="phone"
        label="评测模板编号"
      />
      <el-table-column
        prop="date"
        label="评测时间"
      />
      <el-table-column
        prop="state"
        label="诊断结论"
      />
      <el-table-column
        prop="states"
        label="操作"
      >
        <template>
          <el-button type="primary" size="small">详情</el-button>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
import { mapGetters } from 'vuex'
export default {
  name: 'Index',
  data() {
    return {
      tableData: [
        {
          name: '234234243',
          phone: '13344556677',
          date: '2020-10-30',
          state: '未评测',
          states: '未填写'
        },
        {
          name: '656546465',
          phone: '13344556677',
          date: '2020-10-30',
          state: '评测中',
          states: '已填写'
        },
        {
          name: '868776767',
          phone: '13344556677',
          date: '2020-10-30',
          state: '已出结果',
          states: '未填写'
        }
      ]
    }
  },
  computed: {
    ...mapGetters([
      'avatar'
    ])
  },
  watch: {},
  mounted() {},
  methods: {}
}
</script>

<style scoped lang="scss">
.user-avatar {
  width: 50px;
}
</style>
