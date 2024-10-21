<template>
    <div id="carouselExampleAutoplaying" class="carousel slide" data-bs-ride="carousel">
      <div class="carousel-inner">
        <div v-for="(item, index) in carouselItems" :key="index" class="carousel-item" :class="{ active: index === 0 }">
          <img :src="item.src" class="d-block w-100" :alt="item.alt">
        </div>
      </div>
      <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true" ></span> 
        <span class="visually-hidden">Previous</span>
      </button>
      <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleAutoplaying" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </template>

  <script setup>
import { onMounted } from 'vue';


const carouselItems =  [
    {
        src:'https://www.groups3.com/wp-content/uploads/2020/05/import-products-1-1024x576.jpg',
        alt:''
    }
];

</script>