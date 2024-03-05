<template>
  <div class="home">
    <div class="pop-up-btn" @click="togglePopup">SUBSCRIBE</div>
    <PopupVue :showPopup="showPopup" @closePopup="togglePopup" />
  </div>
</template>

<script>
import PopupVue from "@/components/Popup.vue";
export default {
  name: "HomeView",
  components: {
    PopupVue,
  },
  data() {
    return {
      showPopup: false,
    };
  },
  methods: {
    togglePopup() {
      this.showPopup = !this.showPopup;
    },
  },
};
</script>

<style scoped>
.home {
  width: 100%;
  height: 100vh;
  background-color: #defff3;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
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
