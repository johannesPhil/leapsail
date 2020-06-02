<template>
  <div class="container">
    <Header />
    <div class="hero">
      <div class="hero__text">
        <h1 class="dark-text">
          Our pricing plan for everyone
        </h1>
        <p class="grey-text">Packages are for individuals only</p>
      </div>
      <div class="hero__illustration">
        <img src="./assets/eiffel.svg" alt="" />
      </div>
    </div>
    <div class="plan">
      <div class="plan__option">
        <div id="feat">
          <h2>plan features</h2>
          <ul class="feat__ul">
            <li class="feat__li">Loan</li>
            <li class="feat__li">Investment</li>
            <li class="feat__li">Travel Savings</li>
            <li class="feat__li">Security</li>
            <li class="feat__li">Bank Statement</li>
            <li class="feat__li">Visa</li>
            <li class="feat__li">Ticket</li>
            <li class="feat__li">Escort</li>
            <li class="feat__li">Free Destination</li>
            <li class="feat__li">Tour Package</li>
            <li class="feat__li">Hotel Reservation</li>
            <li class="feat__li">Customer Success</li>
            <li class="feat__li">Travel Show</li>
            <li class="feat__li">Event</li>
            <li class="feat__li">Games</li>
            <li class="feat__li">Gold investor</li>
            <li class="feat__li">Startup</li>
            <li class="feat__li">Give a meal</li>
            <li class="feat__li">Cargo</li>
          </ul>
        </div>
        <div id="bronze">
          <Bronze @toggleBronze="toggleBronze" />
          <ul
            class="bronze__ul"
            ref="bronze__ul"
            :class="{ isVisible: isBronze }"
          >
            <li class="bronze__li">
              <span class="mobile_desc">Loan</span>
              <span>50K - 2M Naira</span>
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Investment</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Travel Savings</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Security</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Bank Statement</span>
              <span>200K - 450K Naira</span>
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Visa</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Ticket</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Escort</span>
              <span>__</span>
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Free Destination</span>
              <span>Just 1</span>
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Tour Package</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Hotel Reservation</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Customer Success</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Travel Show</span>
              <span>__</span>
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Events</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Games</span> <span>__</span>
            </li>
            <li class="bronze__li"><span class="mobile_desc">Gold Investor</span>
              <span>__</span></li>
            <li class="bronze__li"><span class="mobile_desc">Startup</span>
              <span>__</span></li>
            <!-- <li class="bronze__li">__</li> -->
            <li class="bronze__li">
              <span class="mobile_desc">Give a Meal</span>
              
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="bronze__li">
              <span class="mobile_desc">Cargo</span>
            
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
          </ul>
        </div>
        <div id="silver">
          <Silver @toggleSilver="toggleSilver" />
          <ul class="silver__ul" :class="{ isVisible: isSilver }">
            <li class="silver__li">
               <span class="mobile_desc">Loan</span>
              <span>50K - 150K Naira</span>
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Investment</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Travel Savings</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Security</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Bank Statement</span>
              <span>200K - 1M Naira</span>
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Visa</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Ticket</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Escort</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Free Destination</span>
              <span>Just 3</span>
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Tour Package</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Hotel Reservation</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Customer Success</span>
              <span>__</span>
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Travel Show</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Event</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Games</span>
              <span>__</span>
            </li>
            <li class="silver__li">
              Silver Investor
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Startup</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Give a Meal</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="silver__li">
              <span class="mobile_desc">Cargo</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
          </ul>
        </div>
        <div id="gold">
          <Gold @toggleGold="toggleGold" />
          <ul class="gold__ul" :class="{ isVisible: isGold }">
            <li class="gold__li">
              <span class="mobile_desc">Loan</span>
              <span>50K - 4M Naira</span>
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Investment</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Travel Savings</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Security</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Bank Statement</span>
              <span>200K - 1M Naira</span></li>
            <li class="gold__li">
              <span class="mobile_desc">Visa</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Ticket</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Escort</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Free Destination</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Tour Package</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Hotel Reservation</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Customer Success</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Travel Show</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Events</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Games</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Gold Investor</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Startup</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Give a Meal</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
            <li class="gold__li">
              <span class="mobile_desc">Cargo</span>
              <font-awesome-icon :icon="['fas', 'check-circle']" />
            </li>
          </ul>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Bronze from "./components/Bronze";
import Silver from "./components/Silver";
import Gold from "./components/Gold";
import Footer from './components/Footer';
export default {
  name: "App",
  components: {
    Header,
    Bronze,
    Silver,
    Gold,
    Footer
  },
  data() {
    return {
      isBronze: false,
      isSilver: false,
      isGold: false
    };
  },
  methods: {
    toggleBronze(visibility) {
      this.isBronze = visibility;
    },
    toggleSilver(visibility) {
      this.isSilver = visibility;
    },
    toggleGold(visibility) {
      this.isGold = visibility;
    }
  }
};
</script>

<style>
* {
  box-sizing: border-box;
}
html,
body {
  margin: 0;
  padding: 0;
  background-color: #f5f5f5;
  font-family: "Noto Sans JP", sans-serif;
}
img {
  width: 100%;
  height: 100%;
}
.container {
  position: relative;
  margin: 0 auto;
  padding: 0;
  box-sizing: border-box;
  min-height: 100vh;
  overflow: auto;
}

.hero {
  position: relative;
  width: 100%;
  padding-left: 5rem;
  height: 80vh;
  top: 96px;
  display: flex;
  background-color: #fff;
}
.hero__text {
  color: #242424;
}
.grey-text {
  color: #d2d2d2;
}
.hero__illustration {
}
.plan {
  position:relative;
  width: 100%;
  height: auto;
  background-color: #f5f5f5;
}
.plan__option {
  position: relative;
  height: auto;
  overflow: auto;
  top: -5rem;
  padding: 2rem;
  background-color: #fff;
  border-radius: 65px;
  box-shadow: 0px 3px 10px #00000029;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
/* 
#bronze{
  height: auto;
  overflow: auto;
} */
#feat h2 {
  margin: 0;
  text-transform: capitalize;
  width: auto;
  height: 400px;
}
.feat__ul,
.bronze__ul,
.silver__ul,
.gold__ul {
  padding-inline-start: 0;
}
.mobile_desc {
  color: #656565;
}
.feat__li,
.bronze__li,
.silver__li,
.gold__li {
  width: 100%;
  list-style: none;
  height: 4rem;
  text-align: center;
  display: flex;
  flex-direction: row;
  align-items: center;
}
.feat__li {
  text-align: left;
  padding-left: 1rem;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
}
.bronze__li {
  color: #00d154;
}
.silver__li {
  color: #0090e8;
}
.gold__li {
  color: #7a00d1;
}
.feat__li:nth-child(odd),
.bronze__li:nth-child(odd),
.silver__li:nth-child(odd),
.gold__li:nth-child(odd) {
  background-color: #fbfbfb;
}

@media screen and (min-width: 320px) {
  .plan__option {
    left: 5%;
    width: 90%;
    flex-direction: column;
  }
  .hero {
    flex-direction: column;
  }
  .hero__text,
  .hero__illustration {
    width: 100%;
  }
  #feat,
  .feat__ul,
  .bronze__ul,
  .silver__ul,
  .gold__ul {
    display: none;
  }
  .mobile_desc {
    display: block;
  }
  .bronze__li,
  .silver__li,
  .gold__li {
    justify-content: space-between;
  }
  #bronze,
  #silver,
  #gold {
    width: 100%;
  }
}

@media screen and (min-width: 760px) {
  .hero {
    flex-direction: row;
    justify-content: space-between;
  }
  .hero__text {
    width: 20%;
  }
  .hero__illustration {
    width: 70%;
  }
  .plan__option {
    flex-direction: row;
  }
  .mobile_desc {
    display: none;
  }
  .bronze__li,
  .silver__li,
  .gold__li {
    justify-content: center;
  }
  #feat,
  .feat__ul,
  .bronze__ul,
  .silver__ul,
  .gold__ul {
    display: block;
  }
  #feat,
  #bronze,
  #silver,
  #gold {
    width: 25%;
  }
}

@media screen and (min-width: 1000px) {
  .plan__option {
    left: 10%;
    width: 80%;
  }
}
.isVisible {
  display: block;
}
</style>
