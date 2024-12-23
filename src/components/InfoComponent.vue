<template>
  <div class="info-container">
    <div class="info-content">
      <div class="info-header-wrapper">
        <div class="info-header">
          <div class="info-icon">
          <img src="@/components/icons/IconStart.svg" alt="" />
          </div>
        <h1 class="info-title">Новая коллекция <br class="br">французских авторов</h1>
      </div>

      <div class="info-description">
        <p>
          Сложно сказать, почему акционеры <br class="br-d-mobile"> крупнейших компаний призывают <br class="br-d"> нас к новым свершениям,
          которые,<br class="br-d-mobile"> в свою очередь, должны быть <br class="br-d"> заблокированы <br class="br-d"> в рамках своих собственных<br class="br-d-mobile"> рациональных
          ограничений.
        </p>
        <p>
          Принимая во внимание показатели<br class="br-d-mobile"> успешности,<br class="br-d"> граница обучения кадров предопределяет<br class="br-d-mobile"> высокую<br class="br-d">
          востребованность направлений<br class="br-d-mobile"> прогрессивного развития.
        </p>
        <button class="info-button">Ознакомиться</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.info-container {
  position: relative;
  background-image: url('@/assets/promo.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  width: 1440px;
  height: 100%;
  margin: 0 auto;
}

.info-content {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  padding: 0 1.5rem;
  color: white;
  gap: 1.75rem;
  width: 1100px;
  height: 574px;
  margin: 0 auto;
}
.br-d{
  display: none;
}
.br-d-mobile{
  display: none;
}
.info-header-wrapper{
  width: 545px;
  height: 574px;
  display: flex;
  flex-direction: column;
  align-items: start;
  justify-content: center;
}


.info-header {
  display: flex;
  align-items: center;
  gap: 10px;
  margin: 20px 0px;
}

.info-icon {
  margin-right: 10px;
}

.info-title {
  font-family: 'Roboto', sans-serif;
  font-size: 40px;
  color: white;
  
}

.info-description {
  font-family: 'Roboto', sans-serif;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.info-description p {
  font-size: 18px;
  line-height: 1.75;
}

.info-button {
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  background-color: #eedb6d;
  color: black;
  margin: 40px 0px;
  font-weight: 400;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s;
  width: 230px;
  height: 65px;
}

.info-button:hover {
  background-color: #d4b44f;
}
@media screen and (max-width: 690px) {
  .info-button {
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  background-color: #eedb6d;
  color: black;
  margin: 40px 0px;
  font-weight: 400;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s;
  width: 210px;
  height: 50px;
}
.info-container {
width: 690px;
padding: 10px;  
}
}
@media screen and (max-width: 510px) {
  .info-button {
  width: 180px;
  height: 40px;
}
  .info-icon img{
    width: 50px;
  height: 50px;
  }
  .info-title {
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  color: white;
  
}
.info-description {
  white-space: normal;
}
.info-description p {
  font-size: 14px;
  line-height: 1.75;
}
.br-d{
  display: block;
}
}

@media screen and (max-width: 480px) {
  .info-button {
  width: 280px;
  font-size: 16px;
  height: 40px;

}
  .info-icon img{
    width: 50px;
  height: 50px;
  }
  .info-title {
  font-family: 'Roboto', sans-serif;
  font-size: 20px;
  color: white;
  
}
.info-description {
  white-space: normal;
}
.info-description p {
  font-size: 14px;
  line-height: 1.75;
}
.br-d-mobile{
  display: block;
}
}
</style>