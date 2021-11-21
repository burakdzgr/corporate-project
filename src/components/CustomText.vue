<template>
    <component :is="tag" :class="size">
        <slot />
    </component>
</template>


<script>
export default {
    name: 'CustomText',
    props: {
        tag:{
            type: String,
            default: 'span'
        },
        size: {
            type: String,
            default: 'normal'
            
        }
    }
}
</script>

<style scoped>
.small {
    font-size: 12px;
}
.xsmall {
    font-size: 11px;
}
.xxsmall {
    font-size: 10px;
}
</style>