<script setup lang="ts">
import { defineComponent,type PropType } from 'vue';
</script>

<template>
    <button 
        class="button"
        type="submit">
        {{ title }}
    </button>
</template>
;
<style lang="scss">

.button {
    padding: 29px 57px;
    font-size: 16px;
    font-weight: 700;
    line-height: 23px;
    border-radius: 10px;
    border: none;
    background: linear-gradient(#f2da80, #f9d862);
    cursor: pointer;

    &:hover {
        background-color: #FFA722;
    }
}
</style>

<script lang="ts">


export default defineComponent({
    name: 'ButtonComponent',
    components: {

    },
    props: {
        title: {
            type: String,
            default: 'Выбрать Тариф'
        }
    },
})
</script>