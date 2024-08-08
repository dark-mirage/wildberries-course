<script setup lang="ts">
import { defineComponent,type PropType } from 'vue';
</script>

<template>
    <div class="advantages">
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
        flex-wrap: wrap;
        gap: 30px;
    }

    &__item {
        max-width: 378px;
        padding: 32px 18px 50px 47px;
        border-radius: 10px;
        background: rgb(16, 24, 43);
    }

    &__text {
        max-width: 180px;
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

@media(max-width: 1150px) {
    .advantages {
        &__item {
            max-width: 70%;
            width: 100%;
        }

        &__text {
            max-width: 100%;
            font-size: 42px;
        }

        &__span {
            max-width: 100%;
            font-size: 28px;
            line-height: 38px;
        }

        &__img {
            width: 340px;
            height: 257px;
        }
    }
}

@media(max-width: 860px) {
    .advantages {
        &__item {
            max-width: 100%;
            width: 100%;
        }
    }
}

@media(max-width: 600px) {
    .advantages {
        &__text {
            max-width: 100%;
            margin-bottom: 18px;
            font-size: 32px;
        }

        &__span {
            max-width: 100%;
            margin-bottom: 23px;
            font-size: 18px;
            line-height: 28px;
        }

        &__img {
            width: 300px;
            height: 207px;
        }
    }
}

@media(max-width: 460px) {
    .advantages {
        &__text {
            max-width: 100%;
            font-size: 22px;
            line-height: 30px;
        }

        &__span {
            max-width: 100%;
            font-size: 14px;
            line-height: 28px;
        }

        &__img {
            width: 280px;
            height: 187px;
        }

        &__img {
            width: 180px;
            height: 127px;
        }
    }
}

@media(max-width: 400px) {
    .advantages__item {
        padding: 22px 12px 30px 27px;
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