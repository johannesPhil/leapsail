<template>
  <div class="footer">
    <div class="logo">
      <img src="../assets/lit-footer.png" alt="">
    </div>
    <div class="links">
      <a href="">Terms</a>
      <a href="">Careers</a>
      <a href="">Privacy Policy</a>
      <a href="">Leapsail Copyright 2020</a>
    </div>
    <div class="social">
      <font-awesome-icon :icon="['fab', 'instagram']" />
      <font-awesome-icon :icon="['fab', 'twitter']" />
      <font-awesome-icon :icon="['fab', 'facebook-f']" />
      <font-awesome-icon :icon="['fab', 'linkedin']" />
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style scoped>
a {
  display: block;
  padding: 0 1rem;
  text-decoration: none;
  color: #fff;
  font-size: 0.6rem;
  border-left: solid 1px #fff;
}
.footer {
  width: 100%;
  padding: 3rem 1rem;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  background: #242424;
  color: #fff;
}
.logo{
    width: 100px;
    height: 100px;
}
img{
    width: 100%;
    height: 100%;
}
.links,
.social {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}
.links a:nth-child(1) {
  border: transparent;
}
.social {
  width: 30%;
}

@media screen and (min-width: 320px) {
  .footer {
    flex-direction: column;
  }
  .logo,
  .links,
  .social {
    margin: 0.5rem;
  }
}

@media screen and (min-width: 760px) {
  .footer {
    flex-direction: row;
  }
}
</style>
