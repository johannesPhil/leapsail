<template>
  <div class="header">
    <div class="logo">
      <img src="../assets/lit.png" alt="" />
    </div>
    <div class="user-control">
      <font-awesome-icon
        :icon="['fas', 'bell']"
        class="icon--grey"
        style="color: #808D93"
      />
      <p>
        Status: Online
        <font-awesome-icon
          :icon="['fas', 'circle']"
          class="icon--green"
          style="color: #00D154"
        />
      </p>
      <font-awesome-icon
        :icon="['fas', 'user-circle']"
        class="icon--purple"
        style="color: #7A00D1; font-size:2rem"
      />
      <font-awesome-icon
        :icon="['fas', 'ellipsis-v']"
        class="icon--grey"
        style="color: grey"
      />
    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  width: 100%;
  height: 96px;
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 1px 1px 2px #00000005;
  opacity: 1;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  z-index: 2;
}
.logo {
  width: 80px;
  height: 80px;
  margin-left: 2rem;
}
img {
  width: 100%;
  height: 100%;
}
.user-control {
  min-width: 30%;
  margin-right: 2rem;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}
.icon--grey {
  font-size: 1.7rem;
  color: #808d93;
}
</style>
