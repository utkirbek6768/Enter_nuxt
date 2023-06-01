<script>
export default {
  data() {
    return {
      none: false,
    };
  },
};
</script>

<template>
  <div class="wrapper">
    <header class="header">
      <div class="heder-control size-control">
        <Logo />
        <UiNavbar />
        <Personal />
      </div>
    </header>
    <main class="main z-1">
      <Hero />
      <TrainingPrograms />
      <Determination />
      <Directions />
      <Vacancies />
      <Graduates />
    </main>
    <Fotter />
  </div>
</template>
<style>
.heder-control {
  display: flex;
  align-items: center;
  padding: 40px 0px;
}
</style>
