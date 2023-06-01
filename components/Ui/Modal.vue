<template>
  <div
    class="modal-control w-100 h-100 realitiwe flex justify-center align-center m-auto fixed"
  >
    <div @click="hide" class="modal-bg"></div>
    <div class="modal" @click="show">
      <section class="modal-body">
        <slot name="body" />
      </section>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    requird: false,
  },
  methods: {
    hide() {
      this.$emit("hide");
    },
    show() {
      this.$emit("show");
    },
  },
};
</script>
<style>
.modal-control {
  width: 100%;
  height: 100%;
  align-items: center;
  z-index: 99;
  left: 0px;
  top: 0px;
}

.modal-bg {
  position: absolute;
  left: 0px;
  top: 0px;
  width: 100%;
  height: 100%;
  background: rgba(26, 19, 19, 0.5);
}

.modal {
  position: relative;
  background: white;
  border-radius: 25px;
  z-index: 999;
  padding: 20px;
}

.modal__title {
  font-size: 40px;
  margin-left: 5%;
}

.close {
  right: 5%;
  top: 5%;
  transform: rotate(45deg);
  font-size: 40px;
  border-radius: 100%;
  background: red;
  width: 30px;
  height: 30px;
  line-height: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0px;
  padding: 0px;
}
</style>
