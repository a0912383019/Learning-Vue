<template>
    <div>
        <h2>Vue项目</h2>
        <child-com1 :foo="foo" :boo="boo" :coo="coo" :doo="doo" title="前端工程">
        </child-com1>
    </div>
</template>
<script>
const child1 = () => import("./child1.vue");
export default {
    components: { child1 },
    data() {
        return {
            foo: "Javascript",
            boo: "Html",
            coo: "CSS",
            doo: "Vue"
        };
    }
};
</script>
