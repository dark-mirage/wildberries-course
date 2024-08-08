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
    color: #92540c;
    border-radius: 15px;
    box-shadow: 0 2;
    border: none;
    background: linear-gradient(#ffc267, #ffa722);
    background: linear-gradient(#f2da80, #f9d862);
    cursor: pointer;
    box-shadow: 0px 5px 0px 0px #8b7111;

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