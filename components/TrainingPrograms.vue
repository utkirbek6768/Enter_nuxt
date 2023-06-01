<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          index: 1,
          title: "Школьникам",
          bg: "#e4edfa",
          text: "Желающие получить дополнительное образование в IT, дизайне, маркетинге и компьютерной грамотности.",
          link: "",
        },
        {
          id: 2,
          index: 2,
          title: "Профессионалом",
          bg: "#EAE9FB",
          text: "Которые хотят расширить свой кругозор и приобрести новые знания в выбранных областях.",
          link: "",
        },
        {
          id: 3,
          index: 3,
          title: "Студентам",
          bg: "#E5FBF1",
          text: "Желающие получить дополнительное образование в IT, дизайне, маркетинге и компьютерной грамотности.",
          link: "",
        },
        {
          id: 4,
          index: 4,
          title: "Профессионалом",
          bg: "#FBE5E5",
          text: "Которые хотят расширить свой кругозор и приобрести новые знания в выбранных областях..",
          link: "",
        },
        {
          id: 5,
          index: 5,
          title: "Студентам",
          bg: "#E5FBF1",
          text: "Желающие получить дополнительное образование в IT, дизайне, маркетинге и компьютерной грамотности.",
          link: "",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="size-control">
    <div class="section__title">
      Для кого предназначены наши обучающие программы?
    </div>
  </div>
  <div class="trainingPrograms size-control">
    <Swiper
      :modules="[SwiperAutoplay, SwiperEffectCreative]"
      :loop="true"
      :breakpoints="{
        0: { slidesPerView: 1 },
        600: { slidesPerView: 2 },
        920: { slidesPerView: 3 },
        1200: { slidesPerView: 4 },
      }"
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
      <SwiperSlide
        v-for="slide in data"
        :key="slide.id"
        class="trainingPrograms-slider"
      >
        <div
          class="trainingPrograms-card"
          :class="[`aaaa-${slide}`]"
          :style="{ backgroundColor: `${slide.bg}` }"
        >
          <div class="card-img mx-auto mb-3">
            <span class="slider--index" :style="{ color: `${slide.bg}` }">{{
              slide.index
            }}</span>
            <img src="../public/childern-img.png" class="w-full" />
          </div>
          <div class="card__title">{{ slide.title }}</div>
          <div class="card__text">
            {{ slide.text }}
          </div>
        </div>
      </SwiperSlide>
    </Swiper>
  </div>
</template>

<style scoped>
.section__title {
  margin-bottom: 90px;
  max-width: 768px;
}

.trainingPrograms {
  margin-bottom: 90px;
}

.trainingPrograms-card {
  max-width: 338px;
  height: 500px;
  padding: 24px 30px;
  background: #e6edfa;
  border-radius: 40px;
  margin: auto;
}

.card-img {
  background: linear-gradient(
    308.91deg,
    #ffffff 16.12%,
    rgba(255, 255, 255, 0) 95.37%
  );
  border-radius: 20px;
  overflow: hidden;
  position: relative;
}

.card__title {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 140%;
  color: #383838;
  margin-bottom: 20px;
}

.card__text {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #383838;
  opacity: 0.6;
  margin-bottom: 36px;
}

.slider--index {
  font-family: "Mont";
  font-style: normal;
  font-weight: 950;
  font-size: 80px;
  line-height: 140%;
  position: absolute;
  top: 0px;
  right: 10px;
}
@media screen and (max-width: 1500px) {
  .trainingPrograms-card {
    margin-right: 5%;
  }
}
</style>
