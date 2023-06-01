<template>
  <UiModal v-if="showModal" @hide="hide" @show="show" :title="'Modal title'">
    <template #body>
      <form @submit.prevent class="flex gap-7">
        <div class="form-control">
          <label for="pet-select" class="label">Направления</label>

          <select name="directions" id="pet-select">
            <option class="pet-option" value="Все">Все</option>
            <option class="pet-option" value="dog">Dog</option>
            <option class="pet-option" value="cat">Cat</option>
            <option class="pet-option" value="hamster">Hamster</option>
            <option class="pet-option" value="parrot">Parrot</option>
            <option class="pet-option" value="spider">Spider</option>
            <option class="pet-option" value="goldfish">Goldfish</option>
          </select>
        </div>
        <div class="form-control">
          <label for="pet-select" class="label">Уровень сложности</label>

          <select name="directions" id="pet-select">
            <option class="pet-option" value="Любой">Любой</option>
            <option class="pet-option" value="dog">Dog</option>
            <option class="pet-option" value="cat">Cat</option>
            <option class="pet-option" value="hamster">Hamster</option>
            <option class="pet-option" value="parrot">Parrot</option>
            <option class="pet-option" value="spider">Spider</option>
            <option class="pet-option" value="goldfish">Goldfish</option>
          </select>
        </div>
        <div class="form-control">
          <label for="pet-select" class="label">Длителность</label>

          <select name="directions" id="pet-select">
            <option class="pet-option" value="От 1 до 6 месяцов">
              От 1 до 6 месяцов
            </option>
            <option class="pet-option" value="dog">Dog</option>
            <option class="pet-option" value="cat">Cat</option>
            <option class="pet-option" value="hamster">Hamster</option>
            <option class="pet-option" value="parrot">Parrot</option>
            <option class="pet-option" value="spider">Spider</option>
            <option class="pet-option" value="goldfish">Goldfish</option>
          </select>
        </div>
        <div class="form-control">
          <label for="pet-select" class="label">Город</label>

          <select name="directions" id="pet-select">
            <option selected class="pet-option" value="Фергана">Фергана</option>
            <option class="pet-option" value="dog">Dog</option>
            <option class="pet-option" value="cat">Cat</option>
            <option class="pet-option" value="hamster">Hamster</option>
            <option class="pet-option" value="parrot">Parrot</option>
            <option class="pet-option" value="spider">Spider</option>
            <option class="pet-option" value="goldfish">Goldfish</option>
          </select>
        </div>
        <button class="modal-btn" @click="submitHandler">Найти</button>
      </form>
    </template>
  </UiModal>
  <div class="personal-control">
    <button class="personal-btn" @click="show">
      <svg
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle cx="11" cy="11" r="7" stroke="#383838" />
        <path d="M20 20L16 16" stroke="#383838" stroke-linecap="square" />
      </svg>
    </button>
    <button class="personal-btn">uz</button>
    <button class="personal-btn">
      <svg
        width="16"
        height="16"
        viewBox="0 0 16 16"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <g clip-path="url(#clip0_3_38)">
          <path
            d="M10 1H13.3333C13.7754 1 14.1993 1.16389 14.5118 1.45561C14.8244 1.74733 15 2.143 15 2.55556V13.4444C15 13.857 14.8244 14.2527 14.5118 14.5444C14.1993 14.8361 13.7754 15 13.3333 15H10"
            stroke="#383838"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M6 12L10 8L6 4"
            stroke="#383838"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M10 8H1"
            stroke="#383838"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </g>
        <defs>
          <clipPath id="clip0_3_38">
            <rect width="16" height="16" fill="white" />
          </clipPath>
        </defs>
      </svg>
    </button>
    <button class="personal--user__btn">Личный кабинет</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showModal: false,
    };
  },
  methods: {
    hide() {
      this.showModal = false;
    },
    show() {
      this.showModal = true;
    },
    submitHandler() {
      this.showModal = false;
    },
  },
};
</script>
<style scoped>
.form-control {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 5px 16px;
  gap: 2px;
  isolation: isolate;
  width: 233.5px;
  background: #f5f5f5;
  border-radius: 10px;
}

.label {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 140%;
  color: #9b9b9b;
}

select {
  -webkit-appearance: none !important;
  -moz-appearance: none !important;
  -ms-appearance: none !important;
  appearance: none !important;
  outline: 0px !important;
  box-shadow: 0px !important;
  border: 0 !important;
  background: transparent !important;
  background-image: none !important;
}

select::-ms-expand {
  display: none;
}

select {
  position: relative;
  display: flex;
  width: 100%;
  height: 3em;
  line-height: 3;
  background: transparent;
  overflow: hidden;
  border-radius: 0.25em;
}

select {
  flex: 1;
  cursor: pointer;
}

select::after {
  content: "\25BC";
  position: absolute;
  top: 0;
  right: 0;
  background: #383838;
}

.modal-btn {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 1px 80px;
  width: 207px;
  background: #383838;
  border-radius: 10px;

  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  color: #ffffff;
}

.personal-btn {
  width: 40px !important;
  height: 40px !important;
  border-radius: 100%;
  background: #f5f5f5;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 10px;
  border: none;
}

.personal-control {
  display: flex;
  margin-left: auto;
  font-family: "Manrope";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 140%;
  /* or 22px */

  display: flex;
  align-items: center;

  /* Unnamed Color */

  color: #383838;
}

.personal--user__btn {
  display: flex;
  justify-content: center;
  align-items: center;
  background: transparent;
  border: none;
}
</style>
