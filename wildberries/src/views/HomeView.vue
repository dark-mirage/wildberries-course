<script setup lang="ts">
import { defineComponent } from 'vue';
import AdvantagesComponent, { type AdvantagesListItem } from '../components/AdvantagesComponent.vue';
import CourseContentComponent from '../components/CourseContentComponent.vue';
</script>

<template>
  <section>
    <div class="Advantages"> <AdvantagesComponent :AdvantagesItems="AdvantagesItems"/></div>
  </section>
  
  <section>
    <div class="Course-Content"> <CourseContentComponent :items="items"/></div>
  </section>
</template>

<style lang="scss">

section {
  margin-bottom: 40px;
}

</style>

<script lang="ts">

export default {
  name: "HomeView",
  components: {
    AdvantagesComponent,
    CourseContentComponent
  },
  data() {
    return {
      AdvantagesItems: [
        {
          text: 'ИЩЕШЬ УДАЛЕННУЮ РАБОТУ НА ФРИЛАНСЕ',
          span: 'Ты всегда мечтал иметь работу без привязки к месту, и работать из любой точки мира',
          img: 'src/assets/img/img1.png'
        },
        {
          text: 'ХОЧЕШЬ СМЕНИТЬ РАБОТУ НА СВОЕ ДЕЛО',
          span: 'Ты устал работать в найме,хочется перемен и новых возможностей',
          img: 'src/assets/img/img2.png'
        },
        { 
          text: 'ИЩЕШЬ ВОЗМОЖНОСТЬ ЗАРАБАТЫВАТЬ В ДЕКРЕТЕ',
          span: 'Хочешь реализовать свои амбиции и обеспечить своему ребенку будущее',
          img: 'src/assets/img/img3.png'
        }
      ] as AdvantagesListItem[],
      items: [
        {
          module: 'модуль 1',
          text: 'РЕГИСТРАЦИЯ НА МАРКЕТПЛЕЙСЕ И РАБОТА С ДОКУМЕНТАМИ',
          span: 'По итогу модуля вы зарегистрируете ИП/ООО, откроете счет в банке, подберете бухгалтера и зарегистрируете аккаунт поставщика на WildBerries',
          img: 'src/assets/img/document.png'
        },
        {
          module: 'модуль 2',
          text: 'ВЫБОР НИШИ И ПОИСК ТОВАРА ДЛЯ ПРОДАЖИ',
          span: 'В результате модуля ты подберешь востребованный товар, проанализируешь нишу, найдешь поставщика и закупишь первый товар.',
          img: 'src/assets/img/boxes.png'
        },
        { 
          module: 'модуль 3',
          text: 'ПРОДВИЖЕНИЕ ТОВАРОВ НА МАРКЕТПЛЕЙСЕ',
          span: 'Ты научишься продвигать свой товар в ТОП на маркетплейсе и заработаешь первые деньги.',
          img: 'src/assets/img/money.png'
        }
      ]
    }
  },
}

</script>
