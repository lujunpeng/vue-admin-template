<!--
 * @Date: 2020-10-29 16:48:05
 * @LastEditors: lujunpeng
 * @LastEditTime: 2020-10-29 17:31:28
 * @FilePath: /bus_fe_pcweb/Users/lujunpeng/Documents/Code/qbzc/vue-admin-template/src/views/userManagement/index.vue
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
        label="头像"
        width="180"
      >
        <template>
          <img :src="avatar+'?imageView2/1/w/80/h/80'" class="user-avatar">
        </template>
      </el-table-column>
      <el-table-column
        prop="name"
        label="昵称"
        width="180"
      />
      <el-table-column
        prop="phone"
        label="电话"
      />
      <el-table-column
        prop="date"
        label="注册时间"
      />
      <el-table-column
        prop="state"
        label="评测状态"
      />
      <el-table-column
        prop="states"
        label="问卷状态"
      />
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
          name: '张三',
          phone: '13344556677',
          date: '2020-10-30',
          state: '未评测',
          states: '未填写'
        },
        {
          name: '张三',
          phone: '13344556677',
          date: '2020-10-30',
          state: '评测中',
          states: '已填写'
        },
        {
          name: '张三',
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
