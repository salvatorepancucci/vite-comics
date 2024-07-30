<template>
    <div class="col-2 mb-3">
      <div class="card">
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
  
  <style lang="scss" scoped>
  @import './styles/generals.scss';

  .card {
    border: none;
    width: 150px; 
    height: 250px;
    background-color: $secondary-color;
    color: white;
  }

  .card-img-top {
    height: 150px; 
    width: 150px;
    object-fit: cover;
    margin-bottom: 5px;
  }

  .card-body {
    padding: 2px;
  }

  .card-title {
    font-size: 0.875rem; 
    font-weight: bold;
  }

  .card-text {
    font-size: 0.75rem; 
    margin-bottom: 0.25rem;
  }
</style>

  