<template>
  <nav class="navbar-container">
    <div class="navbar">
      <div class="w-fit">
        <img src="../assets/LogoHome.svg" alt="">
      </div>
      <DeviderComponent></DeviderComponent>
      <div class="navbar__links">
        <p class="first-text">Репродукции</p>
        <p class="second-text">Новинки</p>
        <p class="third-text">О нас</p>
        <div class="burger">
          <img src="../assets/List.svg" alt="" class="List">
        </div>
        <div>
          <img src="../assets/CartIcon.svg" alt="" class="cart-icon">
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import DeviderComponent from './DeviderComponent.vue'
</script>

<style scoped>
.navbar {
  display: flex;
  max-width: 1440px;
  width: 100%;
  justify-content: space-between;
  padding: 0 20px;
}
.burger{
  display: none;
}
.navbar-container {
  margin: 0 auto;
  display: flex;
  align-items: center;
  position: static;
  justify-content: center;
  top: 0;
  height: 100px;
  background-color: #e1ede6;
  font-family: 'Roboto', sans-serif;
}

.navbar__links {
  display: flex;
  gap: 60px;
  align-items: center;
  font-size: 24px;
}
.cart-icon{
  display: flex;
  align-items: center;
  width:28px;
  height: 28px;
}

@media screen and (max-width: 690px) {
  .navbar {
    flex-direction: column; 
    align-items: center;
    padding: 10px;
  }
  .navbar-container {
    height: auto;
  }
  .navbar__links {
    gap: 40px;
    font-size: 20px; 
  }

  .cart-icon {
    width: 24px;
    height: 24px; 
  }
}


@media screen and (max-width: 510px) {
  .navbar {
    flex-direction: column; 
    align-items: center;
    padding: 10px 15px; 
    
  }
  
  .navbar__links {
    gap: 30px;
    font-size: 18px; 
    flex-wrap: wrap; 
    justify-content: start;
  }

  .cart-icon {
    width: 20px;
    height: 20px;
    justify-content: end;
  }
}

@media screen and (max-width: 480px) {
  .navbar-container {
    flex-direction: column; 
    align-items: center;
    height: auto; 
    padding: 10px; 
  }
  .burger{
    display: block;

  }
  .first-text{
    display: none;
  }
  .second-text{
    display: none;
  }
  .third-text{
    display: none;
  }
  .navbar__links {
    flex-direction: row; 
    gap: 220px;
  }

  .cart-icon {
    width: 18px;
    height: 18px; 
  }
}

</style>
