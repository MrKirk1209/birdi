<template>
  <div class="hero-container">
    <img src="../assets/HeroImg.png" alt="" class="hero__img" />
    <div class="hero__left-part">
      <div class="hero__content-title">
        <h3 class="hero__title">
          Реплики картин <br />
          от <b class="hero__title-green">Ink. House</b>
        </h3>
        <p class="hero__subtitle">
          Высокое качество отрисовки на плотной бумаге или льняном <br />
          холсте. Редкие произведения, доступные цены.
        </p>
      </div>
      <div class="hero-btn">
        <PrimaryBtn></PrimaryBtn>
      </div>
    </div>
  </div>
</template>

<script setup>
import PrimaryBtn from './PrimaryBtn.vue'
</script>

<style scoped> 
.hero-container {
  max-width: 1440px;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  gap: 30px;
  padding: 0 15px;
  
}
.hero-btn {
  max-width: 225px;
}
.hero__content-title {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.hero__left-part {
  display: flex;
  justify-content: center;
  flex-direction: column;
  gap: 60px;
}

.hero__img {
  width: 540px;
  height: 621px;
}

.hero__title {
  
  font-family: 'Roboto', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 60px;
  line-height: 110%;

  color: #2c2d35;
}

.hero__title-green {
  color: #598d66;
}

.hero__subtitle {
  font-family: 'Roboto', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  color: #86928B;
  line-height: 150%;
}

@media screen and (max-width: 768px) {
  .hero__img {
    width: 330px;
    height: 380px;
  }

  .hero__title {
    font-size: 40px;
  }

  .hero__subtitle {
    font-size: 18px;
  }
}

@media screen and (max-width: 510px) {
  .hero__img {
    width: 195px;
    height: 239px;
  }

  .hero__title {
    font-size: 30px;
  }

  .hero__subtitle {
    font-size: 14px;
  }
  .hero__left-part {
    gap: 10px;
  }
}

@media screen and (max-width: 480px) {
  .hero__img {
    display: none;
  }
  .hero-container {
    margin-top: 30px;
  }
  .hero__title {
    font-size: 26px;
  }

  .hero__subtitle {
    font-size: 12px;
  }
  .hero-btn {
    width: 154px;
    height: 50px; 
    font-size: 14px;
  }
}
</style>
