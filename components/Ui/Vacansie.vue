<template>
  <NuxtLink>
    <div class="vacancies-control">
      <div class="vacansie-item flex justify-around grid grid-cols-12 gap-4">
        <div class="vacansie-avatar md:col-span-1"></div>
        <div
          class="vacansie-title-control col-span-12 sm:col-span-6 md:col-span-5"
        >
          <span class="vacansie__name">Графический Дизайнер</span>
          <span class="compania__name">ООО «UZUM TECHNOLOGIES»</span>
        </div>
        <div
          class="vacansie-title-control col-span-12 sm:col-span-6 md:col-span-5"
        >
          <span class="vacansie__name">от 8 000 000 сумов</span>
          <span class="compania__name">Полная занятость, полный день</span>
        </div>
        <span
          class="next md:col-span-1 flex items-center justify-center ml-auto"
          ><svg
            class="w-100 ml-auto"
            width="50"
            height="25"
            viewBox="0 0 8 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path d="M1 1L7 7L1 13" stroke="#383838" /></svg
        ></span>
      </div>
    </div>
  </NuxtLink>
</template>
<script>
export default {};
</script>
<style scoped>
@media screen and (max-width: 1020px) {
  .vacansie-avatar {
    display: none;
  }
  .vacansie-item {
    text-align: center;
  }
  .next {
    display: none;
  }
}
.vacansie-title-control {
  max-width: 460px;
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.vacansie-item {
  background: #f5f5f5;
  border-radius: 25px;
  padding: 10px;
  margin-bottom: 30px;
  max-width: 1440px;
  margin: auto;
  margin-bottom: 30px;
}
.vacansie-avatar {
  width: 80px;
  height: 80px;
  border-radius: 100%;
  background: #7000ff;
  margin-right: 30px;
}
.vacansie__name {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 140%;
  color: #383838;
}
.compania__name {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #9b9b9b;
}
</style>
