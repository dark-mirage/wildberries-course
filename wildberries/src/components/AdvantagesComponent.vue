<script setup lang="ts">
import { defineComponent,type PropType } from 'vue';
</script>

<template>
    <div class="advantages container">
        <ul class="advantages__list flex">
            <li class="advantages__item flex-column" 
            v-for="(AdvantagesItem, AdvantagesIndex) in AdvantagesItems"
            :key="AdvantagesIndex">
                <p class="advantages__text">
                    {{ AdvantagesItem.text }}
                </p>
                <span class="advantages__span">
                    {{ AdvantagesItem.span }}
                </span>
                <img class="advantages__img" :src="AdvantagesItem.img" alt="pic">
            </li>
        </ul>
    </div>
</template>

<style lang="scss">

.advantages {
    
    &__list {
        display: flex;
        justify-content: center;
        gap: 30px;
    }

    &__item {
        max-width: 378px;
        padding: 32px 18px 50px 47px;
        border-radius: 10px;
        background: rgb(16, 24, 43);
    }

    &__text {
        max-width: 200px;
        margin-bottom: 43px;
        font-size: 32px;
        font-weight: 400;
        line-height: 42px;
        letter-spacing: 5%;
        color: white;
    }

    &__span {
        max-width: 281px;
        margin-bottom: 35px;
        font-size: 18px;
        font-weight: 700;
        line-height: 20px;
        letter-spacing: 5%;
        color: rgb(255, 255, 255);
    }

    &__img {
        width: 240px;
        height: 157px;
    }
}
</style>

<script lang="ts">

export interface AdvantagesListItem {
    text: string;
    span: string;
    img: string;
}

export default defineComponent({
    name: 'AdvantagesComponent',
    components: {

    },
    props: {
        AdvantagesItems: Array as PropType<AdvantagesListItem[]>
    }
})
</script>