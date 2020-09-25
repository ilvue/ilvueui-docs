// 组件api说明 表格
<template>
  <div class="api-wrap">
    <h3>{{title}}</h3>
    <Table :columns="tableHeader" :data="tableData"></Table>
  </div>
</template>

<script>
export default {
  name: "DemoApi",
  props: {
    title: {
      type: String,
      default: '属性'
    },
    tableBody: Array,
    tableHead: String
  },
  computed: {
    tableHeader () {
      return this.tableHead.split("|").map(s => s.replace(/^\s*|\s*$/g, "")).map((v,i) => v = {title:v,key:'name' + i})
    },
    tableData () {
      return this.tableBody.map(str => {
        let data = {}
        str.split("|").map((s, i) => data['name'+ i] = s.replace(/^\s*|\s*$/g, ""))
        return data
      })
    },
  }
}
</script>

<style lang="less">

</style>
