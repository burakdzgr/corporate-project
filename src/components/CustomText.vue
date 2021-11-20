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
            default: 'normal',
            validator: function(value){
                return [
                    'normal',
                    'small',
                    'xsmall',
                    'xxsmal'
                ].indexOf(value) !== -1
            } // normal:14, small:12, xsmall: 11, xxsmall: 10
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