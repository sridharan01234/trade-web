<template>
    <div class="card">
      <img :src="imageUrl" class="card-img-top" :alt="imageAlt">
      <div class="card-body">
        <h5 class="card-title">{{ title }}</h5>
        <p class="card-text">{{ description }}</p>
        <a :href="linkUrl" class="btn btn-primary">{{ linkText }}</a>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CardComponent',
    props: {
      imageUrl: {
        type: String,
        required: true
      },
      imageAlt: {
        type: String,
        default: 'Card image'
      },
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      linkUrl: {
        type: String,
        default: '#'
      },
      linkText: {
        type: String,
        default: 'Go somewhere'
      }
    }
  }
  </script>
  
  <style scoped>
  .card {
    width: 18rem;
    transition: transform 0.3s ease-in-out;
  }
  
  .card:hover {
    transform: scale(1.05);
  }
  
  .card-img-top {
    height: 200px;
    object-fit: cover;
  }
  </style>
  