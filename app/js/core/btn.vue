<template>
    <button :class="[className,cname]">
        <slot/>
    </button>
</template>
<script>
export default {
    data(){
        return {
            className: 'btn' //默认样式
        }
    },
    props: {
        cname: {
            type: String,
            default: ''
        }
    }
}
</script>
<style lang="scss" scoped>
@import '../../css/element.scss';
.btn{
    @include btn;
}
</style>