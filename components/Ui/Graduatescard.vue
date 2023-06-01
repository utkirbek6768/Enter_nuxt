<template>
  <div class="graduatesCard m-auto">
    <div class="graduates-avatar">
      <img src="../../public/childern-img.png" alt="" />
    </div>
    <div class="graduates-text-control">
      <div class="graduates__title">Хожиакбар Анорбоев</div>
      <div class="graduates__text">
        Я окончил курс программирования Python в этой школе и очень доволен
        своим выбором. Курсы были построены очень грамотно, начиная с базовых
        концепций языка и заканчивая созданием собственных проектов.
      </div>
      <span>
        <NuxtLink to="/">Читать историю</NuxtLink>
      </span>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
@media screen and (max-width: 800px) {
  .graduates-avatar {
    width: 40% !important;
    height: 220px;
    position: relative;
    bottom: 0px;
    background: white;
    border-radius: 15px;
    margin-right: 46px;
  }
}
.graduatesCard {
  max-width: 828px;
  height: 338px;
  background: #e6edfa;
  border-radius: 40px;
  padding: 50px;
  display: flex;
  align-items: flex-end;
  margin: auto;
}

.graduates-text-control {
  max-width: 440px;
}

.graduates-text-control span {
  border-bottom: 1px solid black;
  padding-bottom: 5px;
}

.graduates-avatar {
  width: 30%;
  height: 220px;
  position: relative;
  bottom: 0px;
  background: white;
  border-radius: 15px;
  margin-right: 46px;
}

.graduates-avatar img {
  position: absolute;
  bottom: 0px;
  left: 0px;
  border-radius: inherit;
  width: 100%;
}

.graduates__title {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 140%;
  color: #383838;
  margin-bottom: 30px;
}

.graduates__text {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #383838;
  margin-bottom: 42px;
}
</style>
