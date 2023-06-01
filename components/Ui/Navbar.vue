<template>
  <div class="navbar-control">
    <NuxtLink class="navbar__link" to="/"
      >Все курсы
      <svg
        class="inline"
        width="12"
        height="7"
        viewBox="0 0 12 7"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path d="M11 0.5L6 5.5L1 0.500001" stroke="#383838" /></svg
    ></NuxtLink>
    <NuxtLink class="navbar__link" to="/">Акции и скидки</NuxtLink>
    <NuxtLink class="navbar__link" to="/">Вакансии</NuxtLink>
    <NuxtLink class="navbar__link" to="/">О компании</NuxtLink>
    <NuxtLink class="navbar__link" to="/">Контакты</NuxtLink>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.navbar-control {
  display: flex;
}
.navbar__link {
  text-decoration: none;

  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  display: flex;
  align-items: center;

  color: #383838;
  margin-right: 10px;
}
@media screen and (max-width: 968px) {
  .navbar-control {
    display: none;
  }
}
</style>
