<template>
  <div class="silver">
    <h2 class="silver__title">silver</h2>
    <div class="silver__cost">
      <p class="silver__amount">&#8358;&nbsp;2,000</p>
      <p class="silver__frequency">Per month</p>
    </div>
    <button>Activate</button>
    <font-awesome-icon
    class="hide"
      v-if="isVisible"
      :icon="['fas', 'caret-up']"
      @click="toggleSilver"
      style="font-size: 2rem;cursor:pointer; color:#0090e8"
    />
    <font-awesome-icon
    class="hide"
      v-if="!isVisible"
      :icon="['fas', 'caret-down']"
      @click="toggleSilver"
      style="font-size: 2rem;cursor:pointer; color:#0090e8"
    />
  </div>
</template>

<script>
export default {
  name: "Silver",
  data() {
    return {
      isVisible: false
    };
  },
  methods: {
    toggleSilver() {
      this.isVisible = !this.isVisible;
      this.$emit("toggleSilver", this.isVisible);
    }
  }
};
</script>

<style scoped>
.silver {
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
.silver:hover {
  top: -10px;
  box-shadow: 0px 3px 10px #00000029;
}
.silver__title {
  text-transform: uppercase;
  color: #0090e8;
}
.silver__amount {
  color: #656565;
  font-size:3rem;
}
.silver__frequency {
  text-align: center;
  color: #d2d2d2;
}
button {
  width: 80%;
  margin: 0 auto;
  padding: 1rem 3rem;
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
