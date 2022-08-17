<template>
    <div class="border">
        <p>boo: {{ boo }}</p>
        <p>child2: {{ $attrs }}</p>
        <child-com3 v-bind="$attrs"></child-com3>
    </div>
</template>
<script>
const child3 = () => import("./child3.vue");
export default {
    components: {
        child3
    },
    inheritAttrs: false,
    props: {
        boo: String
    },
    created() {
        console.log(this.$attrs);
    }
};
</script>
