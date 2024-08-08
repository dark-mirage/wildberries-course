<script setup lang="ts">
import { defineComponent,type PropType } from 'vue';
import ButtonComponent from './ButtonComponent.vue';
</script>

<template>
    <div class="course-content">
        <ul class="course-price__list flex">
            <li class="course-price__item flex-column" v-for="(PriceItem, PriceIndex) in PriceItems" :key="PriceIndex">
                <p class="course-price__text">
                    {{ PriceItem.text }}
                </p>
                <div class="course-price__divider">
                    <ul class="course-price__item-list gap14px wrap" >
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
                </div>
                <div class="course-price__btn-wrapper flex-column">
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
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        align-items: center;
        gap: 30px;
    }
    
    &__item {
        padding: 46px 0px 54px 0px;
        width: 380px;
        border-radius: 10px;
        background: rgb(21, 31, 54);
    }
    
    &__item-list {
        display: flex;
        flex-direction: column;
        gap: 11px;
        padding: 21px  30px 44px 20px;
    }

    &__text {
        max-width: 205px;
        margin-bottom: 24px;
        padding: 0px 30px 0px 30px;
        font-size: 32px;
        font-weight: 400;
        line-height: 32px;
        color: white;
    }

    &__btn-wrapper {
        gap: 25px;
        padding: 0px 30px 0px 30px;
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
    
    &__divider {
        margin-bottom: 30px;
        border-top: 1px solid rgb(90, 90, 90);
        border-bottom: 1px solid rgb(90, 90, 90);
    }

    &__item:nth-child(2) {
        margin-bottom: 100px;
        background-color: #d9d9d9;
    }
}

.course-price__item:nth-child(2) > .course-price__text  {
    color: black
}

.course-price__item:nth-child(2) > div> ul> li> span {
    color: black;
}

.course-price__item:nth-child(2) .course-price__price-info {
    color: black;
}

.course-price__item:nth-child(2) .course-price__divider {
    border-top: 1px solid rgb(192 192 192);
    border-bottom: 1px solid rgb(192 192 192);
}

@media (max-width: 1400px) {
  .wildberries__second-line-span {
    font-size: 150px;
  }

  .wildberries__second-line-text  {
    font-size: 32px;
  }

  .course-price__item {
    max-width: 70%;
    width: 100%;
  }

  .course-price__text {
    font-size: 44px;
  }

  .course-price__span {
    font-size: 28px;
  }

  .course-price__price-info {
    font-size: 42px;
  }

  .course__price-btn {
    font-size: 26px;
  }
}

@media(max-width: 860px) {
  .course-price__item {
    max-width: 100%;
  }
}

@media(max-width: 540px) {

  .course-price__item {
    padding: 16px 0px 24px 0px;
  }

  .course-price__item-list {
    padding: 11px 30px 24px 20px;
  }

  .course-price__btn-wrapper {
    gap: 15px
  }

  .course-price__divider {
    margin-bottom: 15px;
}

  .course-price__text {
    font-size: 34px;
  }

  .course-price__span {
    font-size: 18px;
  }

  .course-price__price-info {
    font-size: 32px;
  }

  .course__price-btn {
    font-size: 16px;
  }
}

@media(max-width: 460px) {
  .course__price-btn {
    padding: 19px 27px;
  }
}

@media(max-width: 420px) {
.course-price__text {
    font-size: 24px;
  }

  .course-price__span {
    font-size: 14px;
  }

  .course-price__price-info {
    font-size: 22px;
  }

  .course__price-btn {
    font-size: 12px;
  }
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