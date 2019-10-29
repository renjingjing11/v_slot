<template>
    <div class="child">
        <slot name="head" :user="user"></slot>
        内容
        <slot :user="user"></slot>
        <slot name="foot"></slot>
    </div>
</template>
<script>
/**
 * 作用域插槽：可以做一些逻辑操作,使用作用域插槽后，两次调用子组件可以定义不同的渲染方式。
 * 
 * 插槽的一些使用
 * 1.在<slot name="head" :user="user"></slot> 相当于向父子传参数(具名插槽)
 * 2.<slot :user="user"></slot>  相当于向父级传参数(默认插槽)
 */
export default {
    data(){
        return {
            user:{
                name:"任明明",
                age:10
            }
        }
    }
}
</script>