<template>
  <div class="determination">
    <div class="determination-control size-control">
      <div class="determination-form-block">
        <div class="determination__title section__title">
          Разберёмся вместе, какой курс подойдет именно вам
        </div>
        <div class="determination__text">
          Не знаете, какой курс выбрать? Не проблема! Наши эксперты бесплатно
          помогут определиться и ответят на все ваши вопросы. Обучение
          начинается с правильного выбора курса - доверьтесь нам!
        </div>
        <form @submit.prevent class="determination-form grid gap-4">
          <input type="text" class="determination__input" placeholder="Имя" />
          <input
            type="email"
            class="determination__input"
            placeholder="Электронная почта"
          />
          <input
            type="text"
            class="determination__input"
            placeholder="Номер телефона"
          />
          <div class="col-span-11 determination__label">
            Нажимая на кнопку, я соглашаюсь на
            <NuxtLink>
              <span class="determination__span"> обработку персональных </span>
            </NuxtLink>
            данных и
            <NuxtLink
              ><span class="determination__span"
                >с правилами пользования Платформой</span
              ></NuxtLink
            >
          </div>
          <input type="submit" class="btn" />
        </form>
      </div>
      <div
        class="determination-img-block"
        style="
          background: url(../public/next-enter.png);
          background-size: cover;
          background-repeat: no-repeat;
        "
      >
        <NuxtLink to="/"><img src="../public/next-enter.png" /></NuxtLink>
      </div>
    </div>
  </div>
</template>

<style>
.determination {
  margin-bottom: 90px;
}
.determination-control {
  display: flex;
}

.determination__title {
  margin-bottom: 30px;
}

.determination__text {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 140%;
  color: #9b9b9b;
  margin-bottom: 60px;
}

.determination__input {
  width: 100%;
  height: 60px;
  background: #f5f5f5;
  border-radius: 10px;
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #383838;
  padding-left: 20px;
}

.determination-img-block {
  max-width: 529px;
  max-height: 529px;
  margin: auto;
}

.determination-img-block img {
  width: 100%;
  height: 100%;
}

.btn {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1px 80px;
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

.determination__label {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 12px;
  line-height: 140%;
  color: #383838;
}

.determination__span {
  color: #17a2d6;
}
</style>
