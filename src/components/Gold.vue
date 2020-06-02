<template>
  <div class="gold">
    <h2 class="gold__title">gold</h2>
    <div class="gold__cost">
      <p class="gold__amount">&#8358;&nbsp;2,500</p>
      <p class="gold__frequency">Per month</p>
    </div>
    <button>Activate</button>
    <font-awesome-icon
      class="hide"
      v-if="isVisible"
      :icon="['fas', 'caret-up']"
      @click="toggleGold"
      style="font-size: 2rem;cursor:pointer; color:#7a00d1;"
    />
    <font-awesome-icon
      class="hide"
      v-if="!isVisible"
      :icon="['fas', 'caret-down']"
      @click="toggleGold"
      style="font-size: 2rem;cursor:pointer; color:#7a00d1;"
    />
  </div>
</template>

<script>
export default {
  name: "Gold",
  data() {
    return {
      isVisible: false
    };
  },
  methods: {
    toggleGold() {
      this.isVisible = !this.isVisible;
      this.$emit("toggleGold", this.isVisible);
    }
  }
};
</script>

<style scoped>
.gold {
  width: 100%;
  height: 400px;
  padding: 10px 0;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  border-radius: 30px;
  cursor: pointer;
}
.gold:hover {
  top: -10px;
  box-shadow: 0px 3px 10px #00000029;
}
.gold__title {
  text-transform: uppercase;
  color: #7a00d1;
}
.gold__amount {
  color: #656565;
  font-size: 3rem;
}
.gold__frequency {
  text-align: center;
  color: #d2d2d2;
}
button {
  width: 80%;
  margin: 0 auto;
  height: 50px;
  box-shadow: 0px 3px 10px #00000029;
  background-color: #ff6700;
  color: #fff;
  border-radius: 46px;
  border: transparent;
}

@media screen and (max-width: 320px) {
  .hide {
    display: block;
  }
}

@media screen and (min-width: 760px) {
  .hide {
    display: none;
  }
}
</style>
