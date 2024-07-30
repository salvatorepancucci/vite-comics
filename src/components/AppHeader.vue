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
        <div class="container-fluid">
            <div class="row text-center">
                <div class="col-2 p-2 m-2">
                    <img src="../assets/dc-logo.png" alt="Logo">
                </div>
                <div class="col-9 p-2 m-2 d-flex align-items-center justify-content-end">
                    <nav>
                        <ul class="nav fw-bold">
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
@import './styles/generals.scss';

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

header {
    background-color: #fff;
}

.row {
    justify-content: space-between;
}

.nav-link {
    color: $text-dark;
    text-decoration: none;
    font-size: 0.8rem;

    &:hover {
        text-decoration: underline;
    }

    &:visited,
    &:link,
    &:active {
    color: #4d4d4d;
    }
}

</style>