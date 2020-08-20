### 静态滚动列表

<Phone page="page" />

```vue
<template>
  <FlowLader
    ref="loader"
    func="getListByPage"
    type="page"
    :auto="3"
    :query="requestParams"
  >
  </FlowLader>
</template>

<script>
export default {
  computed: {
    requestParams() {
      const { query } = this.$route
      return {
        id: query.id,
        count: 10
      }
    }
  }
}
</script>
```