<template>
  <section class="team-section">
    <div class="image-wrapper">
      <div class="image-container">
          <img src="@/assets/picture.svg" alt="Frame" class="main-image" />
          <img src="@/assets/hand.svg" alt="Hand with Brushes" class="overlay-image" />
        </div>
    </div>
    <div class="text-content">
      <h2>Наша команда</h2>
      <p>
        Значимость этих проблем настолько очевидна, что базовый вектор развития позволяет оценить
        значение экспериментов, поражающих по своей масштабности и грандиозности. Мы вынуждены
        отталкиваться от того, что консультация с широким активом.
      </p>
      <div class="team-icons">
        <div v-for="(member, index) in teamMembers" :key="index" class="icon-container">
          <img :src="member.image" :alt="member.name" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TeamSection',
  data() {
    return {
      teamMembers: [
        { name: 'Member 1', image: 'src/assets/woman-1.png' },
        { name: 'Member 2', image: 'src/assets/man-1.jpg' },
        { name: 'Member 3', image: 'src/assets/man-2.jpg' },
      ],
    };
  },
};
</script>

<style scoped>
.team-section {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 50px;
  padding: 50px 0px;
  width: 1100px;
  margin: 0 auto;
}


.image-wrapper {
  padding: 24px;  

}

.image-container {
  position: relative;
  max-width: 400px;
  width: 100%;
}

.main-image {
  width: 445px;
  height: 450px;
}

.overlay-image {
  position: absolute;
  bottom: 20%;
  left:45%;
  transform: translateX(-50%);
  width: 270px;
  height: 400px;
  object-fit: contain;
}

.text-content{
  display: flex;
  flex-direction: column
}

.text-content h2 {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 16px;
}

.text-content p {
  color: #6b7280;
  line-height: 1.6;
  margin-bottom: 24px;
}

.team-icons {
  display: flex;
  gap: 16px;
  flex-wrap: wrap;
}

.icon-container {
  width: 64px;
  height: 64px;
  border: 2px solid #d1d5db;
  border-radius: 50%;
  overflow: hidden;
}

.icon-container img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

@media (max-width: 690px) {
  .team-section {
    flex-direction: column;
    gap: 30px;
    width: 100%;
    padding: 20px;
    display: flex;
    align-items: start;
  }

  .main-image {
    width: 350px;
    height: 350px;
  }

  .overlay-image {
    width: 200px;
    height: 300px;
  }

  .text-content h2 {
    font-size: 20px;
  }

  .text-content p {
    font-size: 14px;
  }
  .overlay-image {
  position: absolute;
  bottom: 20%;
  left:40%;
  transform: translateX(-50%);
  object-fit: contain;
}
}

@media (max-width: 510px) {
  .team-section {
    padding: 15px;
  }

  .main-image {
    width: 280px;
    height: 280px;
  }

  .overlay-image {
    width: 180px;
    height: 250px;
  }

  .text-content h2 {
    font-size: 18px;
  }

  .text-content p {
    font-size: 12px;
  }

  .team-icons {
    gap: 10px;
  }

  .icon-container {
    width: 50px;
    height: 50px;
  }
}

@media (max-width: 480px) {
  .team-section {
    padding: 10px;
  }

  .main-image {
    width: 240px;
    height: 240px;
  }

  .overlay-image {
    width: 150px;
    height: 220px;
  }

  .text-content h2 {
    font-size: 16px;
  }

  .text-content p {
    font-size: 10px;
  }

  .icon-container {
    width: 40px;
    height: 40px;
  }
  .team-section {
    flex-direction: column;
    gap: 30px;
    width: 100%;
    padding: 20px;
    display: flex;
    align-items: center;
  }
  .overlay-image {
  position: absolute;
  bottom: 20%;
  left:42%;
  transform: translateX(-50%);
  object-fit: contain;
}
}
</style>
