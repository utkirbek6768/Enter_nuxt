<template>
  <div class="graduates">
    <div class="graduates-control size-control">
      <div class="graduates-titleControl flex items-center justify-between">
        <div class="graduates__title section__title">
          Отзывы наших выпускников
        </div>
        <div class="PrevNext-control flex items-center justify-between gap-4">
          <span class="flex items-center justify-center">
            <svg
              width="8"
              height="14"
              viewBox="0 0 8 14"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M7 1L1 7L7 13" stroke="#383838" />
            </svg>
          </span>
          <span class="flex items-center justify-center">
            <svg
              width="8"
              height="14"
              viewBox="0 0 8 14"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M1 1L7 7L1 13" stroke="#383838" />
            </svg>
          </span>
        </div>
      </div>
      <div class="graduates__text">
        Мы гордимся нашими студентами, которые проходят обучение у нас и
        достигают своих целей. Они делятся своими успехами и впечатлениями,
        помогая другим принять решение о выборе курсов.
      </div>
      <div class="graduates-card-control gap-8">
        <Swiper
          :modules="[SwiperAutoplay, SwiperEffectCreative]"
          :breakpoints="{
            0: { slidesPerView: 1 },
            1420: { slidesPerView: 1.7 },
          }"
          :loop="true"
          :autoplay="{
            delay: 8000,
            disableOnInteraction: true,
          }"
        >
          <swiper-slide v-for="slide in 3">
            <UiGraduatescard />
          </swiper-slide>
        </Swiper>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
@media screen and (max-width: 1420px) {
  .graduates-card-control::before {
    content: none !important;
  }
}
.graduates {
  margin-bottom: 243px;
}

.graduates-titleControl {
  margin-bottom: 30px;
}

.graduates-card-control {
  position: relative;
  display: flex;
}

.graduates-card-control::before {
  content: "";
  height: 100%;
  z-index: 9;
  position: absolute;
  right: -5%;
  box-shadow: -100px 1px 100px 150px white;
}

.PrevNext-control span {
  width: 40px;
  height: 40px;
  background: #f5f5f5;
  border-radius: 100%;
}

/* .graduates__text {
  max-width: 768px;
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 140%;
  color: #9b9b9b;
  margin-bottom: 60px;
} */
</style>
