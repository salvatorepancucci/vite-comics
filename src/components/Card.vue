<template>
    <div class="col-md-3 mb-3">
      <div class="card h-100">
        <img :src="thumb" class="card-img-top" :alt="series">
        <div class="card-body">
          <h5 class="card-title">{{ series }}</h5>
          <p class="card-text">{{ type }}</p>
          <p class="card-text">{{ price }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Card',
    props: {
      thumb: String,
      price: String,
      series: String,
      type: String
    }
  }
  </script>
  
  <style scoped>
  .card {
    border: none;
  }
  
  .card-title {
    font-size: 1rem;
    font-weight: bold;
  }
  
  .card-text {
    font-size: 0.875rem;
  }
  </style>
  