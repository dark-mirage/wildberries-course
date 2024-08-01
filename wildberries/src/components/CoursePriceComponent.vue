<script setup lang="ts">
import { defineComponent,type PropType } from 'vue';
import ButtonComponent from './ButtonComponent.vue';
</script>

<template>
    <div class="course-content container">
        <ul class="course-price__list flex">
            <li class="course-price__item flex-column" v-for="(PriceItem, PriceIndex) in PriceItems" :key="PriceIndex">
                <p class="course-price__text">
                    {{ PriceItem.text }}
                </p>
                <ul class="flex-column gap14px wrap" style="padding: 21px  0 44px 0;">
                    <li>
                        <span class="course-price__span">
                            {{ PriceItem.span1 }}
                        </span>
                    </li>
                    <li>
                        <span class="course-price__span">
                            {{ PriceItem.span2 }}
                        </span>
                    </li>
                    <li>
                        <span class="course-price__span">
                            {{ PriceItem.span3 }}
                        </span>
                    </li>
                    <li>
                        <span class="course-price__span">
                            {{ PriceItem.span4 }}
                        </span>
                    </li>
                </ul>
                <div class="course-price__btn-wrapper flex-column" style="gap: 25px">
                    <i class="course-price__price-info">{{ PriceItem.i }}</i>
                    <ButtonComponent class="course__price-btn" title="Выбрать Тариф"/>
                </div>
            </li>
        </ul>
    </div>
</template>

<style lang="scss">

.course-price {
    &__list {
        align-items: center;
        justify-content: center;
        gap: 30px;
    }
 
    &__item {
        max-width: 380px;
        width: 100%;
        padding: 46px 30px 54px 30px;
        border-radius: 10px;
        background: rgb(21, 31, 54);
    }

    &__text {
        max-width: 205px;
        font-size: 32px;
        font-weight: 400;
        line-height: 32px;
        color: white;
    }

    &__span {
        font-size: 18px;
        font-weight: 350;
        line-height: 27px;
        color: rgb(255, 255, 255);
    }
    
    &__price-info {
        font-size: 32px;
        font-weight: 400;
        line-height: 32px;
        color: white;
    }

    &__item:nth-child(2) {
        margin-bottom: 100px;
        background-color: #d9d9d9;
    }
}

.course-price__item:nth-child(2) > .course-price__text  {
    color: black
}

.course-price__item:nth-child(2) > ul> li> span {
    color: black;
}

.course-price__item:nth-child(2) .course-price__price-info {
    color: black;
}

</style>

<script lang="ts">

export interface PriceListItem {
    module: string;
    text: string;
    span1: string;
    span2: string;
    span3: string;
    span4: string;
    i: string;
}

export default defineComponent({
    name: 'CourseContentComponent',
    components: {
        ButtonComponent
    },
    props: {
        PriceItems: Array as PropType<PriceListItem[]>
    },
})
</script>