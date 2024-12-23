<template>
  <footer class="footer-container">
    <div class="footer-content">
      <div class="footer-section">
        <div class="footer-logo-text">
          <div class="footer-logo">
          <img src="../assets/LogoHome.svg" alt="" class="hero__img" />
        </div>
        <div class="footer-text">
          <h2 class="footer-heading-text">+7 (999) 543-54-54</h2>
          <p class="footer-item-text">Мастерская</p>
        </div>
        </div>
      </div>
      <div class="footer-links-desktop">
        <div class="link-group">
          <h2 class="footer-heading-text">Репродукции</h2>
          <p class="footer-item-text">Франция</p>
          <p class="footer-item-text">Германия</p>
          <p class="footer-item-text">Англия</p>
        </div>
        <div class="link-group">
          <h2 class="footer-heading-text">Новинки</h2>
          <p class="footer-item-text">2021</p>
          <p class="footer-item-text">2020</p>
        </div>
        <div class="link-group">
          <h2 class="footer-heading-text">О нас</h2>
          <p class="footer-item-text">Художники</p>
          <p class="footer-item-text">Менеджеры</p>
        </div>
      </div>
      <div class="footer-mobile">
        <div class="footer-logo">
            <div class="footer-logo">
            <img src="../assets/LogoHome.svg" alt="" class="hero__img" />
            </div>
        </div>
  <div class="footer-text-main">
      <div class="footer-text-1">
        <div class="footer-text">
          <h2 class="footer-heading-text">+7 (999) 543-54-54</h2>
          <p class="footer-item-text">Мастерская</p>
        </div>
            <div class="footer-links-mobile">
              <div class="link-group">
                <h2 class="footer-heading-text">Новинки</h2>
                <p class="footer-item-text">2021</p>
                <p class="footer-item-text">2020</p>
              </div>
            </div>
        </div>
      
      <div class="footer-text-2">
              <div class="link-group">
                <h2 class="footer-heading-text">Репродукции</h2>
                <p class="footer-item-text">Франция</p>
                <p class="footer-item-text">Германия</p>
                <p class="footer-item-text">Англия</p>
              </div>
              <div class="link-group">
                <h2 class="footer-heading-text">О нас</h2>
                <p class="footer-item-text">Художники</p>
                <p class="footer-item-text">Менеджеры</p>
              </div>
            </div>
  </div>      
      </div>
 
      <DeviderComponent></DeviderComponent>

      <div class="social-media">
        <div class="social-icons">
          <img src="@/components/icons/IconFacebook.svg" alt="footer-icon" class="footer-icon" />
          <img src="@/components/icons/IconInstagram.svg" alt="footer-icon" class="footer-icon" />
          <img src="@/components/icons/IconYouTube.svg" alt="footer-icon" class="footer-icon" />
        </div>
        <div class="legal-info">
          <p class="footer-links">Ink. House ®</p>
          <p class="footer-links">All rights reserved</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import DeviderComponent from './DeviderComponent.vue';
</script>

<style scoped>
.footer-container {
  background-color: #e1ede6;
  padding: 25px 15px;
  display: flex;
  justify-content: center;
}

.footer-content {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
  width: 1440px;
}

.footer-mobile{
  display: none;
}
.footer-section {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

.footer-logo-text {
  display: flex;
  flex-direction: column;
  padding: 0 40px;
}

.footer-links-desktop{
    display: flex;
    flex-direction: row;
    align-items: start;
    width: 100%;
    padding: 0 80px;
    gap: 40px;
}

.social-media {
  display: flex;
  flex-direction: column;
  gap: 10px;
  padding: 0 100px;
}

.social-icons {
  display: flex;
  gap: 15px;
}

.footer-heading-text {
  font-size: 20px;
  font-weight: 500;
  line-height: 23px;
  white-space: nowrap;
  color: var(--black-text);
}

.footer-item-text {
  font-size: 18px;
  line-height: 150%;
  font-weight: 500;
  color: var(--gray-text);
}

.footer-links {
  font-size: 12px;
  font-weight: 500;
  line-height: 120%;
  color: var(--gray-text);
}

.footer-icon {
  width: 24px;
  height: 24px;
  padding: 3px;
}
@media screen and (max-width: 690px) {
  .footer-content {
    display: flex;
    flex-direction: column;
  }
  .footer-logo-text {
    display: flex;
    flex-direction: row;
    gap: 200px;
    align-items: center;
  }
  .footer-links-desktop {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .social-media {
    display: block;
  }

}

@media screen and (max-width: 510px) {
  .footer-container {
    padding: 20px 10px;
  }
  .footer-content {
    flex-direction: column;
    gap: 15px;
    align-items: center;
  }
  .footer-links-mobile {
    gap: 10px;
  }
  .footer-heading-text {
    font-size: 18px;
    line-height: 21px;
  }
  .footer-item-text {
    font-size: 16px;
  }
  .footer-links {
    font-size: 10px;
  }
}

@media screen and (max-width: 480px) {
  .footer-container {
    padding: 20px 10px;
    background-color: #e1ede6;
  }
  .footer-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    width: 100%;
  }
  .footer-logo-text {
    display: none;
  }
  .footer-links-desktop {
    display: none;
  }
  .social-media {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }
  .footer-mobile{
    display: block;

  }
  .footer-text-main{
    display: flex;
    flex-direction: row;
    gap: 70px;
  }
  .footer-text-1{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 50px;
  }
  .footer-text-2{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 50px;
  }
}
@media screen and (max-width: 320px) {
  .footer-container {
    padding: 20px 10px;
    background-color: #e1ede6;
  }
  .footer-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    width: 100%;
  }
  .footer-logo-text {
    display: none;
  }
  .footer-links-desktop {
    display: none;
  }
  .social-media {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
  }
  .footer-mobile{
    display: block;

  }
  .footer-text-main{
    display: flex;
    flex-direction: row;
    gap: 45px;
  }
  .footer-text-1{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 50px;
  }
  .footer-text-2{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 50px;
  }
}

</style>