<template>
  <div class="container">
    <div class="row">
      <div class="col-md-2 mb-3 d-flex">
        <div class="card h-100">
          <img :src="thumb" class="card-img-top" :alt="series">
          <div class="card-body">
            <h5 class="card-title">{{ series }}</h5>
            <p class="card-text">{{ type }}</p>
          </div>
        </div>
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
  width: 100%;
  background-color: $secondary-color;
  color: white;
}

.card-img-top {
  height: 150px;
  width: 100%; 
  object-fit: cover;
  margin-bottom: 5px;
}

.card-body {
  padding: 10px;
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
