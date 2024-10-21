<template>
    <div class="container mt-5 ">
      <h2 class="mb-4">Contact Us</h2>
      <form @submit.prevent="submitForm">
        <div class="row">
            <div class="mb-3 col-4">
          <label for="name" class="form-label">Name</label>
          <input 
            type="text" 
            class="form-control" 
            id="name" 
            v-model="form.name" 
            required
          >
        </div>
        <div class="mb-3 col-4">
          <label for="email" class="form-label">Email address</label>
          <input 
            type="email" 
            class="form-control" 
            id="email" 
            v-model="form.email" 
            required
          >
        </div>
        <div class="mb-3 col-4">
          <label for="phone" class="form-label">Phone Number</label>
          <input 
            type="tel" 
            class="form-control" 
            id="phone" 
            v-model="form.phone" 
            required
          >
        </div>
        </div>
        <div class="mb-3">
          <label for="message" class="form-label">Message</label>
          <textarea 
            class="form-control" 
            id="message" 
            rows="3" 
            v-model="form.message" 
            required
          ></textarea>
        </div>
        <button type="submit" class="btn btn-primary">Submit</button>
      </form>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ContactUsComponent',
    data() {
      return {
        form: {
          name: '',
          email: '',
          phone: '',
          message: ''
        }
      }
    },
    methods: {
      submitForm() {
        // Here you would typically send the form data to your backend
        console.log('Form submitted:', this.form);
        // Reset form after submission
        this.form = {
          name: '',
          email: '',
          phone: '',
          message: ''
        };
        // You could also show a success message to the user here
      }
    }
  }
  </script>
  
  <style scoped>
  /* Add any custom styles here */
  </style>
  