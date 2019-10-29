<template>
  <div class="parent">
      <Child>
        <template v-slot:head="scope">{{scope.user.name}}</template>
        <template #default="scope">{{scope.user.age}}</template>
        <template v-slot:foot>底部</template>
      </Child>
  </div>
</template>
<script>
/**
 * 在引入子组件的时候,加入要使用子组件的插槽必须使用template标签
 * scope:是子组件传递的data数据
 * 具名插槽：v-slot:head="scope" 
 * 默认插槽：#default="scope"
 */
import Child from './components/child'
export default {
  components:{
    Child
  }
}
</script>
