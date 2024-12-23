<template>
  <div class="card">
    <div class="pic-img-wrapper">
      <img :src="imageSrc" alt="image" />
    </div>
    <div class="card-content">
      <p class="picture-title">{{ props.author }}</p>
      <div class="card-text-wrapper">
        <h2 class="card-text-header">{{ props.title }}</h2>
        <h3 class="card-desc">{{ props.description }}</h3>
      </div>
      <div class="card-footer">
        <p class="card-price">{{ props.price }} руб</p>
        <PrimaryBtn text="В корзину"></PrimaryBtn>
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'
import PrimaryBtn from './PrimaryBtn.vue'
const imageSrc = computed(() =>
  props.image ? `images/${props.image}` : '/placeholder.jpg'
);
const props = defineProps({
  author: {
    type: String,
    default: 'author',
  },
  title: {
    type: String,
    default: 'title',
  },
  price: {
    type: Number,
    default: 0,
  },
  description: {
    type: String,
    default: 'description',
  },
  image: {
    type: String,
    default: 'image',
  },
})

</script>

<style scoped>
.card {
  background-color: #e1ede6;
  padding: 20px;
  max-width: 350px;
  height: 100%;
  width: 100%;
  max-height: 730px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.pic-img-wrapper {
  width: 100%;
  height: auto;
}

.img-responsive {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.picture-title {
  margin-top: 20px;
  font-family: 'Raleway', sans-serif;
  font-weight: 500;
  font-size: 18px;
  line-height: 21px;
  color: #86928b;
}

.card-content {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.card-text-wrapper {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.card-text-header {
  font-family: 'Raleway', sans-serif;
  font-size: 30px;
  color: rgb(44, 45, 53);
  font-weight: 500;
  line-height: 35px;
}

.card-desc {
  font-family: 'Raleway', sans-serif;
  font-size: 18px;
  line-height: 28px;
  color: #444;
}

.card-footer {
  display: flex;
  flex-direction: column;
  gap: 10px;
  width: 100%;
}

.card-price {
  font-family: 'Raleway', sans-serif;
  font-size: 24px;
  font-weight: 500;
  color: rgb(89, 141, 102);
  margin-top: 10px;
}

@media screen and (max-width: 690px) {
  .card {
    max-width: 300px;
    max-height: 730px;
    display: flex;
    padding: 20px;

  }
  .pic-img-wrapper  {
  height: auto;

}
  .pic-img-wrapper img {
  width: 260px;
  height: auto;
  
}
}

@media screen and (max-width: 510px) {
  .card {
    width: 200px;
    height: 525px;
    display: flex;
    padding: 20px;

  }
  .pic-img-wrapper  {
  height: auto;

  }
  .pic-img-wrapper img {
  width: 160px;
  height: auto;
  
  }
  .card-text-header {
    font-size: 14px;
  }
  .card-desc {
    font-size: 11px;
  }
  .card-footer {
    gap: 5px;
  }
  .card-price {
    font-size: 14px;
  }
}

@media screen and (max-width: 480px) {
  .card {
    width: 200px;
    height: 525px;
    display: flex;
    padding: 20px;

  }
  .pic-img-wrapper  {
  height: auto;

  }
  .pic-img-wrapper img {
  width: 160px;
  height: auto;
  
  }
  .card-text-header {
    font-size: 14px;
  }
  .card-desc {
    font-size: 11px;
  }
  .card-footer {
    gap: 5px;
  }
  .card-price {
    font-size: 14px;
  }
}
</style>