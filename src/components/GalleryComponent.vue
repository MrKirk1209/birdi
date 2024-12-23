<template>
  <div class="gallery-container">
    <div class="gallery-header">
      <h1 class="gallery-title">Репродукции</h1>
      <div class="gallery-filters">
        <button
          class="gallery-btn"
          :class="{ active: btnActiveIndex === 0 }"
          @click="handleFilter(0)"
        >
          Франция
        </button>
        <button
          class="gallery-btn"
          :class="{ active: btnActiveIndex === 1 }"
          @click="handleFilter(1)"
        >
          Германия
        </button>
        <button
          class="gallery-btn"
          :class="{ active: btnActiveIndex === 2 }"
          @click="handleFilter(2)"
        >
          Англия
        </button>
      </div>
    </div>
    <div class="gallery-grid">
      <PictureCard
        :key="item.title"
        v-for="item in cards[selectedFilter]"
        :author="item.author"
        :title="item.title"
        :description="item.description"
        :price="item.price"
        :image="item.image"
      ></PictureCard>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import PictureCard from './PictureCard.vue';
import { cards } from '@/const/data';

const btnActiveIndex = ref(0);

const filters = {
  0: 'france',
  1: 'germany',
  2: 'england',
};
const selectedFilter = ref('france');

const handleFilter = (index) => {
  btnActiveIndex.value = index;
  selectedFilter.value = filters[btnActiveIndex.value];
};
</script>

<style scoped>
.gallery-container {
  display: flex;
  flex-direction: column;
  width: 1440px;
  margin: 0 auto;
}


.gallery-header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  gap: 20px;
  position: relative;
  width: 1110px;
  margin: 0 auto;
}



.gallery-title {
  font-size: 40px;
  position: relative;
}

.gallery-filters {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 20px;
  overflow-x: auto;
  padding-top: 10px;
}


.gallery-btn {
  width: 126px;
  height: 43px;
  font-size: 20px;
  border-radius: 20px;
  background-color: #c3d1c6; 
  color: #000;
  border: none;
  cursor: pointer;
  flex-shrink: 0;
  transition: background-color 0.3s, color 0.3s;
}

.gallery-btn.active {
  background-color: #4caf50; 
  color: #fff;
}

.gallery-grid {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  gap: 20px;
  margin: 40px;
  justify-content: center;
}


.scrollbar-hide {
  -ms-overflow-style: none; 
  scrollbar-width: none; 
}

.scrollbar-hide::-webkit-scrollbar {
  display: none; 
}
@media screen and (max-width: 690px) {
  .gallery-container {
    width: 100%;
    padding: 0 10px;
  }

  .gallery-header {
    flex-direction: row;
    align-items: center;
    gap: 10px;
    width: 85%;
  }

  .gallery-title {
    font-size: 26px;
  }

  .gallery-filters {
    flex-wrap: wrap;
    gap: 40px;
    justify-content: center;
  }

  .gallery-btn {
    width: auto;
    padding: 10px 15px;
    font-size: 18px;
  }

  .gallery-grid {
    margin: 20px 10px;
    gap: 15px;
  }
}

@media screen and (max-width: 510px) {
  .gallery-container {
    width: 100%;
    padding: 0 10px;
  }

  .gallery-header {
    flex-direction: column;
    align-items: start;
    gap: 10px;
    width: 85%;
  }

  .gallery-title {
    font-size: 26px;
  }

  .gallery-filters {
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
  }

  .gallery-btn {
    width: auto;
    padding: 10px 15px;
    font-size: 14px;
  }

  .gallery-grid {
    margin: 20px 10px;
    gap: 15px;
  }
}

@media screen and (max-width: 480px) {
 .gallery-container {
    width: 100%;
    padding: 0 10px;
  }

  .gallery-header {
    flex-direction: column;
    align-items: start;
    gap: 10px;
    width: 85%;
  }

  .gallery-title {
    font-size: 26px;
  }

  .gallery-filters {
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
  }

  .gallery-btn {
    width: auto;
    padding: 10px 15px;
    font-size: 14px;
  }

  .gallery-grid {
    margin: 20px 10px;
    gap: 15px;
  }
}
</style>