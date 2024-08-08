<script setup lang="ts">
import { defineComponent } from 'vue';
import AdvantagesComponent, { type AdvantagesListItem } from '../components/AdvantagesComponent.vue';
import CourseContentComponent, {type ContentListItem} from '../components/CourseContentComponent.vue';
import CoursePriceComponent, { type PriceListItem } from '../components/CoursePriceComponent.vue';
import ButtonComponent from '../components/ButtonComponent.vue';
</script>

<template>
  <section class="wildberries section">
    <div class="wildberries__container container">

      <div class="wildberries__wrapper">

        <div class="wildberries__first-line flex">
   
          <div class="wildberries__course-start flex gap10px">  
            <img class="wildberries__icon" src="../assets/img/youtube.svg" alt="youtube icon">
            <div class="flex-column gap4px">
              <span class="wildberries__first-line-span">старт обучения:</span>
              <span class="wildberries__first-line-span-2">22 ФЕВРАЛЯ</span>
            </div>
          </div>
  
          <span class="wildberries__first-line-span">Курс по заработку на маркетплейсах</span>
  
          <div class="wildberries__course-start-2-wrapper flex gap10px">
            <div class="wildberries__course-start-2 flex-column gap4px">
              <span class="wildberries__first-line-span">
                Длительность 
              </span>
              <span class="wildberries__first-line-span-2">
                1 месяц
              </span>
            </div>
            <img class="wildberries__icon" src="../assets/img/time.svg" alt="time icon">
          </div>
        </div>
  
          <div class="wildberries__second-line">
            <p class="wildberries__second-line-text">
              НАУЧИСЬ ЗАРАБАТЫВАТЬ ОТ <strong class="wildberries__second-line-strong">70 000 РУБЛЕЙ</strong> В МЕСЯЦ НА
            </p>
            <span class="wildberries__second-line-span">WILDBERRIES</span>
          </div>

          <div class="wildberries__third-line wildberries-1920px flex">
            <div class="wildberries__third-line-block">
              <h3 class="wildberries__third-line-h3">ЗА 1 МЕСЯЦ ВЫ УЗНАЕТЕ:</h3>
              <p class="wildberries__third-line-text">
                как зарабатывать от 70 000 р. <br>
                в месяц на маркетплейсах
                с помощью проверенных методов
                от практикующего эксперта
              </p>
            </div>

            <div class="wildberries__third-line-block">
              <h3 class="wildberries__third-line-h3">━ АЛЕКСЕЙ ФЕДОРОВ</h3>
              <p class="wildberries__third-line-text">
                Экспер в теме маркетплейсов.
                Более 7 лет опыта. Владелец
                магазина с оборотом 5 млн рублей.
              </p>
            </div>
          </div>
            
          <div class="wildberries__bg">
            <div class="wildberries__btn-wrapper">
              <ButtonComponent class="wildberries__btn" title="ПРИОБРЕСТИ КУРС"/>
            </div>
         </div>

        </div>
   </div>
  </section>

  <section class="advantages section">
    <div class="wildberries__third-line wildberries-960px flex">
            <div class="wildberries__third-line-block">
              <h3 class="wildberries__third-line-h3">ЗА 1 МЕСЯЦ ВЫ УЗНАЕТЕ:</h3>
              <p class="wildberries__third-line-text">
                как зарабатывать от 70 000 р. <br>
                в месяц на маркетплейсах
                с помощью проверенных методов
                от практикующего эксперта
              </p>
            </div>

            <div class="wildberries__third-line-block">
              <h3 class="wildberries__third-line-h3">━ АЛЕКСЕЙ ФЕДОРОВ</h3>
              <p class="wildberries__third-line-text">
                Экспер в теме маркетплейсов.
                Более 7 лет опыта. Владелец
                магазина с оборотом 5 млн рублей.
              </p>
            </div>
      </div>
    
    <div class="advantages__container container">
      <h2 class="advantages__h2 section__h2">ТЕБЕ ПОДОЙДЕТ КУРС, ЕСЛИ</h2>
      <AdvantagesComponent :AdvantagesItems="AdvantagesItems"/>
    </div>
  </section>

  <section class="course-content section">
    <div class="course-content__container container">
      <h2 class="course-content__h1 section__h2">ЧТО БУДЕТ НА КУРСЕ?</h2>
      <CourseContentComponent :ContentItems="ContentItems"/>
    </div>
  </section>

  <section class="price-question section">
    <div class="bg-color">
      <article class="price">
        <div class="price__container container">
          <h2 class="price__h2 section__h2">
            СТОИМОСТЬ КУРСА
          </h2>
          <CoursePriceComponent :PriceItems="PriceItems"/>
        </div>
       </article>
    
      <article class="question">
        <div class="question__container container">
          <h2 class="question__h2 section__h2">ОСТАЛИСЬ ВОПРОСЫ?</h2>
          <span class="question__span">Оставьте свои контакты и мы свяжемся с вами в ближайшие дни</span>
          <form class="question__form" action="#">
            <input class="question__input" type="tel" placeholder="Введите номер" required>
            <input class="question__input" type="email" placeholder="Введите свой E-mail" required>
            <ButtonComponent class="question__btn" title="ЗАДАТЬ ВОПРОС"/>
          </form>
        </div>
      </article>
    </div>

  </section>
  
</template>

<style lang="scss">

body {
  background-color: #171f32;
  background-image: url('src/assets/img/wb-bg.png');
  background-position: center;
  background-size: cover;
}

.section {
  margin-bottom: 100px;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 25px;
}

.section__h2 {
  margin-bottom: 60px;
  font-size: 48px;
  font-weight: 400;
  line-height: 48px;
  color: white;
}

.price {
  margin-bottom: 200px;
}

.question__h2 {
  margin-bottom: 10px;
}

.question__span {
  margin-bottom: 42px;
  font-size: 18px;
  font-weight: 350;
  line-height: 27px;
  color: #dbdbdb;
}

.question__form {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 30px;
  max-width: 1190px;
  width: 100%;
}

.question__input {
  width: 378px;
  padding: 33px 44px 34px 44px;
  background-color: #141f36;
  border: none;
  border-radius: 10px;
}

.question__input::placeholder {
  font-size: 18px;
  font-weight: 400;
  line-height: 26px;
  color: #cbcbcb;
}

.question__btn {
  width: 378px;
  padding: 33px 91px 34px 81px;
  color: #92540c;
  font-size: 16px;
  font-weight: 700;
  line-height: 23px;
}

.price-question {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  margin: 0;
}

.bg-color {
  max-width: 1700px;
  width: 100%;
  padding-top: 100px;
  padding-bottom: 100px;
  border-radius: 25px;
  background-color: #10182b
}

.wildberries__btn-wrapper {
  display: flex;
  justify-content: center;
  width: 100%;
}

.wildberries {
  &__container {
    position: relative;
    width: 100%;
    height: 1216px;
    padding-top: 40px;
    padding: 35px 30px;
    background-image: url('src/assets/img/wildberries-bg.png');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
  }

  &__wrapper {
    max-width: 1207px;
    width: 100%;
  }

  &__bg {
    position: absolute;
    right: 50%;
    top: 25%;
    display: flex;
    justify-content: space-between;
    height: 1027px;
    width: 590px;
    background-image: url('src/assets/img/wildberries-man.png');
    background-position: bottom 200px;
    background-repeat: no-repeat;
    transform: translate(50%, 0);
  }

  &__first-line {
    width: 100%;
    justify-content: space-between;
    margin-bottom: 76px;
  }

  &__icon {
    width: 30px;
    height: 30px;
  }

  &__first-line-span {
    font-size: 14px;
    font-weight: 400;
    line-height: 20px;
    color: #5f5f5f;
  }
  
  &__first-line-span-2 {
    color: #fff;
    font-size: 14px;
    font-weight: 400;
    line-height: 20px;
  }

  &__second-line {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  &__second-line-text {
    font-size: 42px;
    font-weight: 400;
    line-height: 42px;
    color: #fff;
  }

  &__second-line-strong {
    color: #F2DA80
  }

  &__second-line-span {
    font-size: 190px;
    font-weight: 400;
    line-height: 222px;
    color: #F2DA80;
  }

  &__third-line {
    display: flex;
    justify-content: space-between;
  }

  &__third-line-block {
    display: flex;
    flex-direction: column;
    width: 305px;
  }

  &__third-line-h3 {
    margin-bottom: 10px;
    font-size: 18px;
    font-weight: 700;
    line-height: 26px;
    color: #fff;
  }

  &__third-line-text {
    font-size: 18px;
    font-weight: 400;
    line-height: 24px;
    color: #dbdbdb;
  }

  &____btn-wrapper {
    position: relative;
  }

  &__btn {
    position: absolute;
    top: 500px;
    width: 370px;
    font-size: 16px;
    font-weight: 700;
    line-height: 23px;
    border-radius: 20px;
    color: #92540c;
  }

}

.wildberries-960px {
  display: none;
}

@media(max-width: 1400px) { 
  .course-price__item:nth-child(2) {
      margin-bottom: 0px;
      background-color: #d9d9d9;
  }
}

@media(max-width: 1450px) {
  .wildberries__second-line-text {
    font-size: 36px;
  }

  .wildberries__second-line-span {
    font-size: 170px;
}
}

@media(max-width: 1300px) {
  .wildberries__second-line-text {
    font-size: 32px;
  }

  .wildberries__second-line-span {
    font-size: 150px;
    line-height: 190px
  }

  .wildberries__container {
    height: 1116px;
}

  .wildberries__bg {
    top: 26%;
    height: 827px;
  }
}

@media(max-width: 1100px) {

  .wildberries__container {
    height: 1016px;
  }

  .wildberries__bg {
    top: 28.5%;
    height: 727px;
    background-position: center;
    background-size: contain;
  }

  .wildberries__second-line-span {
    font-size: 130px;
  }

  .wildberries__second-line-text {
    font-size: 30px;
  }
}

@media(max-width: 960px) {
  .wildberries-1920px {
    display: none;
  }

  .wildberries-960px {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 50px;
    padding: 50px;
  }

  .wildberries-960px > .wildberries__third-line-block:nth-child(2) {
    margin-left: auto;
  }

  .wildberries__third-line-block {
    max-width: 100%;
    justify-content: flex-end;
  }

  .wildberries__second-line-span {
    font-size: 110px;
  }

  .wildberries__container {
    height: 800px;
  }

  .wildberries__btn {
    top: 470px;
  }

  .wildberries__bg {
    top: 36%;
    height: 527px;
  }

  .wildberries__second-line-span {
    font-size: 95px;
    line-height: 120px;
  }

  .wildberries__second-line-text {
    line-height: 32px;
    
}
}

@media(max-width: 760px) {

  .wildberries__container {
    height: 700px;
    padding: 35px 20px;
  }

  .wildberries__bg {
    top: 39%;
    height: 427px;
  }

  .wildberries__second-line-span {
    font-size: 85px;
  }

  .wildberries__btn {
    top: 380px;
  }

  .wildberries-960px {
    padding: 20px;
  }

  .wildberries__third-line-text {
    max-width: 260px;
  }
  
}

@media(max-width: 640px) {
  .wildberries__second-line-text {
    max-width: 360px;
    font-size: 24px;
    text-align: center;
  }
}

@media(max-width: 600px) {

  .wildberries__first-line {
    display: grid;
    grid-template-areas:
    "wildberries__first-line-span wildberries__first-line-span"
    "wildberries__course-start wildberries__course-start-2";
    grid-gap: 10px;
    grid-template-columns: 300px 1fr;
  }

  .wildberries__first-line-span {
    display: flex;
    grid-area: wildberries__first-line-span;
    justify-content: center;
  }

  .wildberries__course-start {
    grid-area: wildberries__course-start;
  }

  .wildberries__course-start-2-wrapper {
    justify-content: flex-end;
  }

  .wildberries__course-start-2 {
    grid-area: wildberries__course-start;
  }

  .wildberries__second-line-span {
    font-size: 85px;
  }

  .wildberries__bg {
    width: 100%;
  }

  .course-content__item {
    position: relative;
    max-width: 990px;
    padding: 47px 42px 77px 42px;
    border-radius: 10px;
    background: rgb(16, 24, 43);
  }

  .wildberries__first-line {
    margin-bottom: 46px;
}

  .wildberries__wrapper {
    width: 100%;
  }

  .wildberries__container {
    padding: 35px 10px;
  }

  .wildberries__second-line {
    max-width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .section__h2 {
    font-size: 38px;
  }
}

@media(max-width: 520px) {

  .course-content__item {
    position: relative;
    max-width: 990px;
    padding: 47px 32px 77px 32px;
    border-radius: 10px;
    background: rgb(16, 24, 43);
  }

  .course-content__text {
    font-size: 28px;
  }

  .course-content__span {
    font-size: 14px;
  }

  .course-content__img:nth-child(2) {
    width: 300px;
    height: 217px;
}
}

@media(max-width: 500px) {
  .wildberries__second-line-span {
    font-size: 65px;
  }

  .wildberries__first-line { 
    grid-template-columns: 250px 1fr;
  }

  .section__h2 {
    font-size: 32px;
  }
}

</style>

<script lang="ts">

export default {
  name: "HomeView",
  components: {
    AdvantagesComponent,
    CourseContentComponent,
    CoursePriceComponent,
    ButtonComponent
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
      ContentItems: [
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
      ] as ContentListItem[],
      PriceItems: [
        {
          text: 'ЭКОНОМ',
          span1: '- Все модули курса',
          span2: '-  Без проверки Д/З',
          span3: '-  Без дополнительных материалов',
          span4: '-  Без обратной связи',
          i: '4.900 рублей'
        },
        {
          text: 'ПРОФФЕСИОНАЛ',
          span1: '- Все модули курса',
          span2: '-  Дополнительные материалы',
          span3: '-  Дополнительные материалы',
          span4: '-  Обратная связь от кураторов',
          i: '7.900 рублей'
        },
        {
          text: 'ВИП',
          span1: '- Все модули курса',
          span2: '- Проверка Д/З лично автором курса',
          span3: '- Дополнительные материалы',
          span4: '- Обратная связь от автора курса',
          i: '13.900 рублей'
        }
      ] as PriceListItem[],
    }
  },
}

</script>
