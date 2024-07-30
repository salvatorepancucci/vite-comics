<script>
    export default {
        name: 'AppHeader',
        data() {
            return {
                menuItems: ['CHARACTERS', 'COMICS', 'MOVIES', 'TV', 'GAMES', 'COLLECTIBLES', 'VIDEOS', 'FANS', 'NEWS', 'SHOP']
            }
        }
    }
</script>

<template>
    <header>
        <div class="container">
            <div class="row">
                <div class="col-2 p-2 m-2">
                    <img src="../assets/dc-logo.png" alt="Logo">
                </div>
                <div class="col-9 p-2 m-2 d-flex align-items-center ml-auto">
                    <nav>
                        <ul class="nav">
                            <li v-for="(item, index) in menuItems" :key="index" class="nav-item">
                            <a class="nav-link" href="#">{{ item }}</a>
                            </li>
                        </ul>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>

</style>