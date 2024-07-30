<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      sections: [
        {
          title: "DC COMICS",
          items: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
        },
        {
          title: "DC",
          items: ["Terms Of Use", "Privacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contact Us"]
        },
        {
          title: "SITES",
          items: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
        },
        {
          title: "SHOP",
          items: ["Shop DC", "Shop DC Collectibles"]
        }
      ]
    }
  }
}
</script>

<template>
    <footer>
      <div class="footer-top">
        <div class="container">
          <div class="row">
            <div class="col-1 mt-4" v-for="(section, index) in sections" :key="index">
              <h6>{{ section.title }}</h6>
              <ul class="list-unstyled">
                <li v-for="(item, index) in section.items" :key="index">{{ item }}</li>
              </ul>
            </div>
            <div class="col-8 m-4">
                <img src="../assets/dc-logo-bg.png" alt="DC Logo">
            </div>
          </div>
        </div>
      </div>
      <div class="footer-down">
        <div class="container">
          <div class="row d-flex">
            <div class="col-6 mt-4 mb-4">
              <button>
                sign-up now!
              </button>
            </div>
            <div class="col-6 mt-4 mb-4 d-flex">
              <button id="follow">
                follow us
              </button>
              <div><img src="../assets/footer-facebook.png" alt="Facebook"></div>
              <div><img src="../assets/footer-twitter.png" alt="Twitter"></div>
              <div><img src="../assets/footer-youtube.png" alt="Youtube"></div>
              <div><img src="../assets/footer-pinterest.png" alt="Pinterest"></div>
              <div><img src="../assets/footer-periscope.png" alt="Periscope"></div>
            </div>
          </div>
        </div>
      </div>
    </footer>
</template>

<style lang="scss" scoped>
@import './styles/generals.scss';

footer {
    background-image: url('../assets/footer-bg.jpg');
    position: relative;
}

.footer-down {
    position: relative;
    z-index: 3;
    background-color: $secondary-color;
}

.row {
    display: flex;
    justify-content: flex-start;
}

.col-1 {
    font-size: 0.5rem;    
    
    h6 {
      color: white;
    }

    li {
      color: rgb(193, 193, 193);
    }
}

.col-6 {
    justify-content: flex-end;

    img {
      width: 20px;
      position: relative;
      z-index: 4;
      top: 0%;
      right: 0%;
    }
}

img {
    width: 400px;
    position: absolute;
    z-index: 1;
    bottom: 60px;
    right: 200px;
    padding: 2px;
}

button {
    border: 2px solid #0C7CEC;
    background-color: transparent;
    color: #ffffff;
    padding: 5px 8px;
    font-size: 0.7rem;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    cursor: pointer;
}

#follow {
    color: $primary-color;
    background-color: transparent;
    border: none;
    font-size: 0.8rem;
    font-weight: bold;
    text-transform: uppercase;
    cursor: pointer;
}

</style>