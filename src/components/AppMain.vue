<script>
import Card from './Card.vue';

export default {
  name: 'AppMain',
  components: {
    Card
  },
  data() {
    return {
      comics: [
        { "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg", "price": "$19.99", "series": "Action Comics", "type": "comic book" },
        { "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg", "price": "$3.99", "series": "American Vampire 1976", "type": "comic book" },
        { "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg", "price": "$16.99", "series": "Aquaman", "type": "graphic novel" },
        { "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg", "price": "$2.99", "series": "Batgirl", "type": "comic book" },
        { "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg", "price": "$3.99", "series": "Batman", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg", "price": "$2.99", "series": "Batman Beyond", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg", "price": "$3.99", "series": "Batman/Superman", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg", "price": "$4.99", "series": "Batman/Superman Annual", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg", "price": "$5.99", "series": "Batman: The Joker War Zone", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg", "price": "$6.99", "series": "Batman: Three Jokers", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg", "price": "$4.99", "series": "Batman: White Knight Presents: Harley Quinn", "type": "comic book" },
        { "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg", "price": "$16.99", "series": "Catwoman", "type": "graphic novel" }
      ],
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
    <main>
        <div class="jumbotron"></div>
        <div class="container-fluid">
            <div class="row">
                <div class="col-12">
                    <h6 class="text-center">Current Series</h6>
                    <div class="container">
                        <div class="row">
                            <Card
                            v-for="(comic, index) in comics"
                            :key="index"
                            :thumb="comic.thumb"
                            :series="comic.series"
                         />  
                        </div>
                    </div>
                    <div class="text-center mt-3 mb-4">
                        <button class="btn btn-primary">Load More</button>
                    </div>
                </div>
            </div>
        </div>
    </main>
        <div id="primary" class="row">
            <div class="col-8 text-center p-2 d-flex align-items-center">
                <div class="col">
                    <img src="../assets/buy-comics-digital-comics.png" alt="Digital Comics">
                    <span>DIGITAL COMICS</span>
                </div>
                <div class="col">
                    <img src="../assets/buy-comics-merchandise.png" alt="DC Merchandise">
                    <span>DC MERCHANDISE</span>
                </div>
                <div class="col">
                    <img src="../assets/buy-comics-subscriptions.png" alt="Subscription">
                    <span>SUBSCRIPTION</span>
                </div>
                <div class="col">
                    <img src="../assets/buy-comics-shop-locator.png" alt="Shop Locator">
                    <span>COMIC SHOP LOCATOR</span>
                </div>
                <div class="col">
                    <img src="../assets/buy-dc-power-visa.svg" alt="DC Power Visa">
                    <span>DC POWER VISA</span>
                </div>    
            </div>
        </div>
    
</template>

<style lang="scss" scoped>
@import './styles/generals.scss';

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

#dark {
    background-color: $secondary-color;
    color: $text-light;
    height: 100px;
}

#primary {
    background-color: $primary-color;
    height: 150px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-size: 0.8rem;
    position: relative;
    z-index: 2;

    img {
        width: 40px;
        margin-right: 5px;
    }
}

.jumbotron {
    background-image: url('../assets/jumbotron.jpg');
    height: 300px;
    margin-bottom: 20px;
}

.card {
    background-color: $secondary-color;
}

h6 {
    background-color: $primary-color;
    color: white;
    padding: 5px;
    width: 150px;
    position: relative;
    z-index: 7;
    bottom: 35px;
    left: 40px;
    text-transform: uppercase;
    border-radius: 3%;
}

.btn {
    border-radius: 3%;
    width: 120px;
}

</style>