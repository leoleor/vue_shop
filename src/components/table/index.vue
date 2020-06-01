<template>
  <el-table :data=tableData border stripe>
    <template v-for="item in tableColumns">
      <!-- 插槽 -->
      <!-- <el-table-column :key="item.field" :label="item.label" :prop="item.field" v-if="item.columnType==='slot'">
        <template v-solt="scope">
          <slot :name="item.slotName" :data="scope.row"></slot>
        </template>
      </el-table-column> -->

      <!-- 普通 -->
      <el-table-column :key="item.field" :label="item.label" :prop="item.field">
      </el-table-column>
    </template>
  </el-table>
</template>

<script>
export default {
  props: {
    tableColumns: {
      // 表头数据
      type: Array,
      default: () => {
        return []
      }
    },
    tableData: {
      // 表格数据
      type: Array,
      default: () => {
        return []
      }
    },
    scope: {
      // 表格数据
      type: Array,
      default: () => {
        return []
      }
    }
  },
  methods: {
  }
}
</script>