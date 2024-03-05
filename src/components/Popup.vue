<template>
  <div v-if="showPopup" class="popup-div">
    <div class="popup">
      <div class="align-right-div">
        <div class="close-btn" @click="closePopup">&#10006;</div>
      </div>
      <div class="inside">
        <p class="title">SUBSCRIBE!</p>
        <p class="exp">
          Subscribe to our newsletter and get 20% off your first purchase!
        </p>
        <input type="text" class="input" placeholder="Email" />
        <div class="pop-up-btn" @click="closePopup">SUBSCRIBE</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "PopupVue",
  props: {
    showPopup: Boolean,
  },
  methods: {
    closePopup() {
      this.$emit("closePopup");
    },
  },
};
</script>

<style scoped>
.popup-div {
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.2);
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
}
.popup {
  width: 700px;
  height: 530px;
  border-radius: 30px;
  background-image: url("../assets/image.png");
  background-size: contain;
  box-sizing: border-box;
  padding: 24px;
  display: flex;
  flex-direction: column;
  row-gap: 24px;
  align-items: center;
}
.align-right-div {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: end;
}
.close-btn {
  color: white;
  font-size: 24px;
  cursor: pointer;
}
.inside {
  width: 90%;
  height: 400px;
  background-color: white;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  row-gap: 24px;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
  padding: 24px;
}
.title {
  font-size: 60px;
  font-weight: 600;
}
.exp {
  font-size: 16px;
  font-weight: 500;
}
.input {
  box-sizing: border-box;
  width: 100%;
  height: 40px;
  border: none;
  border-radius: 50px;
  background-color: #f3f3f3;
  padding: 16px;
  font-style: italic;
}
.pop-up-btn {
  padding: 16px 48px;
  background-color: #ff487a;
  border-radius: 50px;
  font-weight: 500;
  font-size: 20px;
  color: white;
  cursor: pointer;
  transition: all 0.15s;
}
.pop-up-btn:hover {
  opacity: 0.9;
}
.pop-up-btn:active {
  opacity: 0.8;
}
</style>
