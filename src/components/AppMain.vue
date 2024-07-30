<script>
    export default {
        name: 'AppMain',
        data() {
            return {
            }
        }
    }
</script>

<template>
    <main>
        <div class="container-fluid">
            <div id="dark" class="row">
                <div class="col-8 text-center p-2 d-flex align-items-center justify-content-center">
                    <h4>-> Content goes here <-</h4>
                </div>
            </div>
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
        </div>
    </main>
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

    img {
        width: 40px;
        margin-right: 5px;
    }
}
</style>