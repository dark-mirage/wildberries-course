<script setup lang="ts">
import { defineComponent,type PropType } from 'vue';
</script>

<template>
    <div class="course-content">
        <ul class="course-content__list flex-column">
            <li class="course-content__item flex" v-for="(ContentItem, ContentIndex) in ContentItems" :key="ContentIndex">
                <div class="flex-column">
                    <span class="course-content__module">
                        {{ ContentItem.module }}
                    </span>
                    <p class="course-content__text">
                        {{ ContentItem.text }}
                    </p>
                    <span class="course-content__span">
                        {{ ContentItem.span }}
                    </span>
                </div>
                <img class="course-content__img" :src="ContentItem.img" alt="pic">
            </li>
        </ul>
    </div>
</template>

<style lang="scss">

.course-content {
    &__list {
        align-items: center;
        justify-content: center;
        gap: 30px;
    }

    &__item {
        position: relative;
        max-width: 990px;
        padding: 47px 72px 77px 72px;
        border-radius: 10px;
        background: rgb(16, 24, 43);
    }

    &__module {
        position: absolute;
        top: -18px;
        padding: 9px 27px;
        font-size: 18px;
        font-weight: 400;
        line-height: 18px;
        color: #091225;
        border-radius: 5px;
        background-color: #F2DA80;
    }

    &__text {
        max-width: 540px;
        margin-bottom: 13px;
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

    &__img:first-child {
        width: 297px;
        height: 237px;
    }

    &__img:nth-child(2) {
        width: 388px;
        height: 217px;
    }

    &__img:nth-child(3) {
        width: 335px;
        height: 194px;
    }
}

@media(max-width: 1400px) {
    .course-content__item {
        max-width: 70%;
        width: 100%;
    }
}

@media(max-width: 1270px ) {
    .course-content__item {
        display: flex;
        flex-direction: column;
        gap: 30px;
    }

    .course-content__item:first-child > .course-content__img {
        width: 300px;
    }
} 

@media(max-width: 930px) {
.course-content__item {
    display: flex;
    flex-direction: column;
}

.course-content__span {
    margin-bottom: 40px;
}

.course-content__img {
    width: 280px ;
}
}

@media(max-width: 860px) {
    .course-content__item {
        max-width: 100%;
        width: 100%;
    }
}

@media(max-width: 570px) {
    .course-content__item {
    
    }
}
</style>

<script lang="ts">

export interface ContentListItem {
    module: string;
    text: string;
    span: string;
    img: string;
}

export default defineComponent({
    name: 'CourseContentComponent',
    components: {

    },
    props: {
        ContentItems: Array as PropType<ContentListItem[]>
    },
})
</script>