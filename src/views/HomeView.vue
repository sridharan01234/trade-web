<script setup>
import   HeaderComponent from '../components/HeadeComponent.vue';
import CarosuelComponent from '../components/CarosuelComponent.vue';
import CardComponent from '../components/CardComponent.vue';
import ContactComponent from '../components/ContactComponent.vue';
import FooterComponent from '../components/FooterComponent.vue';


const cards = [
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
        {
          imageUrl: '/path/to/image1.jpg',
          imageAlt: 'Image 1',
          title: 'Card 1',
          description: 'Description for Card 1',
          linkUrl: '/link1',
          linkText: 'Learn More'
        },
      ]

</script>

<template>
    <HeaderComponent />

      <CarosuelComponent />

<div class="container">
  <div class="card-container">
    <CardComponent 
      v-for="(card, index) in cards" 
      :key="index"
      :imageUrl="card.imageUrl"
      :imageAlt="card.imageAlt"
      :title="card.title"
      :description="card.description"
      :linkUrl="card.linkUrl"
      :linkText="card.linkText"
    />
  </div>

  <div class="container">

    <ContactComponent />
  </div>

  <FooterComponent />

</div>
</template>

<style scoped>
.card-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(18rem, 1fr));
  gap: 1rem;
  padding: 1rem;
}
</style>