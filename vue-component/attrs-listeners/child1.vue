<template>
    <div>
        <p>foo: {{ foo }}</p>
        <p>child1的$attrs: {{ $attrs }}</p>
        <child-com2 v-bind="$attrs"></child-com2>
    </div>
</template>
<script>
const child2 = () => import("./child2.vue");
export default {
    components: {
        child2
    },
    inheritAttrs: false, // 可以关闭自动挂载到组件根元素上的没有在props声明的属性
    props: {
        foo: String // foo作为props属性绑定
    },
    created() {
        console.log(this.$attrs);
    }
};
</script>
