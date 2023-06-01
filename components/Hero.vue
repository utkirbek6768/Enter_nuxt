<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          index: 1,
          title: "Хожиакбар Анорбоев",
          bg: "#e4edfa",
          text: "Бросил таксистскую работу и стал программистом благодаря нашему курсу обучения. Начните карьеру в IT-индустрии с нуля с нашими преподавателями и материалами.",
          link: "",
        },
        {
          id: 2,
          index: 2,
          title: "Хожиакбар Анорбоев",
          bg: "#EAE9FB",
          text: "Бросил таксистскую работу и стал программистом благодаря нашему курсу обучения. Начните карьеру в IT-индустрии с нуля с нашими преподавателями и материалами..",
          link: "",
        },
        {
          id: 3,
          index: 3,
          title: "Хожиакбар Анорбоев",
          bg: "#E5FBF1",
          text: "Бросил таксистскую работу и стал программистом благодаря нашему курсу обучения. Начните карьеру в IT-индустрии с нуля с нашими преподавателями и материалами.",
          link: "",
        },
        {
          id: 4,
          index: 4,
          title: "Хожиакбар Анорбоев",
          bg: "#FBE5E5",
          text: "Бросил таксистскую работу и стал программистом благодаря нашему курсу обучения. Начните карьеру в IT-индустрии с нуля с нашими преподавателями и материалами.",
          link: "",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="hero size-control grid grid-cols-2">
    <div class="hero-text-block pl-14">
      <div class="section__title hero__title">
        Изучайте языки программирования
      </div>
      <p class="hero__text">
        Изучайте языки программирования, создавайте приложения и веб-сайты.
        Получите практические навыки.
      </p>

      <form @submit.prevent class="hero-form">
        <input
          type="text"
          class="hero__input"
          placeholder="Курс или профессия"
        />
        <input type="submit" class="hero__button" />
      </form>
    </div>
    <div class="hero-slider-blo">
      <Swiper
        :modules="[SwiperAutoplay, SwiperEffectCreative]"
        :slides-per-view="1"
        :loop="true"
        :autoplay="{
          delay: 8000,
          disableOnInteraction: true,
        }"
        :creative-effect="{
          prev: {
            shadow: false,
            translate: ['-20%', 0, -1],
          },
          next: {
            translate: ['100%', 0, 0],
          },
        }"
      >
        <SwiperSlide v-for="slide in data" :key="slide.id">
          <div class="trainingPrograms-card realitive">
            <div class="hero-slider-img card-img mx-auto mb-3">
              <img src="../public/teacher-avatar.png" class="w-full" />
            </div>
            <div class="card-text-control">
              <div class="card__title">{{ slide.title }}</div>
              <div class="card__text">
                {{ slide.text }}
              </div>
            </div>
          </div>
        </SwiperSlide>
      </Swiper>
    </div>
  </div>
</template>

<style scoped>
.hero {
  background: #c9e7f2;
  border-radius: 40px;
  width: auto;
  margin-bottom: 90px;
}

.hero__title {
  margin-bottom: 20px;
  margin-top: 90px;
}

.hero__text {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 140%;
  color: #383838;
  margin-bottom: 60px;
}

.hero-form {
  padding: 30px;
  background: #ffffff;
  border-radius: 20px;
  display: flex;
}

.hero__input {
  width: 368px;
  height: 60px;
  background: #f5f5f5;
  border-radius: 10px;
  border: none;
  margin-right: 10px;
  padding-left: 5%;
}

.hero__button {
  width: 207px;
  height: 60px;
  background: #383838;
  border-radius: 10px;
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #ffffff;
}

.hero-slider-img {
  max-width: 575px;
  height: 100%;
  margin: auto;
  margin-top: 32px;
}

.hero-slider-img img {
  width: 100%;
  height: 100%;
  position: relative;
  bottom: 0px;
}

.card-text-control {
  position: absolute;
  left: 20%;
  bottom: 126px;
  max-width: 100%;
  max-width: 460px;
  margin: auto;
}

.card__title {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #383838;
  margin-bottom: 11px;
}

.card__text {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 140%;
  color: #383838;
}
@media screen and (max-width: 1150px) {
  .hero {
    align-items: flex-end;
    overflow: hidden;
  }
  .hero-text-block {
    padding-bottom: 60px;
  }
  .trainingPrograms-card {
    height: 100%;
  }
  .hero__title {
    font-size: 40px;
    margin-top: 40px;
  }
  .card-text-control {
    margin: auto !important;
    left: 10%;
    bottom: 20%;
  }
  .hero__input {
    width: 100%;
    height: 60px;
    background: #f5f5f5;
    border-radius: 10px;
    border: none;
    margin-right: 10px;
    padding-left: 5%;
  }
}
@media screen and (max-width: 950px) {
  .hero {
    display: block;
    flex-direction: column;
  }
  .hero-text-block {
    margin: auto;
    padding: 2% 2% 0% 2%;
  }
  .hero__title {
    font-size: 30px;
  }
  .hero-form {
    padding: 2%;
    border-radius: 15px;
  }
}
@media screen and (max-width: 576px) {
  .hero-form {
    padding: 2%;
    border-radius: 15px;
  }
  .hero__text {
    margin-bottom: 5%;
  }
}
</style>
