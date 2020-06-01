<template>
  <div class="bronze">
    <h2 class="bronze__title">Bronze</h2>
    <div class="bronze__cost">
      <p class="bronze__amount">&#8358;&nbsp;500</p>
      <p class="bronze__frequency">Per month</p>
    </div>
    <button>Activate</button>
    <font-awesome-icon
      :icon="['fas', 'caret-down']"
      @click="toggleBronze"
      style="font-size: 2rem;cursor:pointer"
    />
  </div>
</template>

<script>
export default {
  name: "Bronze",
  data() {
    return {
      isVisible: false
    };
  },
  methods: {
    toggleBronze() {
      this.isVisible = true;
      this.$emit("clickBronze", this.isVisible);
    }
  }
};
</script>

<style scoped>
.bronze {
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
.bronze:hover {
  box-shadow: 0px 3px 10px #00000029;
}
.bronze__title {
  text-transform: uppercase;
  color: #00d154;
}
.bronze__amount {
  color: #656565;
}
.bronze__frequency {
  color: #d2d2d2;
  text-align: center;
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
</style>
