<!-- JS -->
<script>
export default {
    name: "AppHeader",
    data() {
        return {
            links: [
                { text: "CHARACTERS", url: "#characters" },
                { text: "COMICS", url: "#comics" },
                { text: "MOVIES", url: "#movies" },
                { text: "TV", url: "#tv" },
                { text: "GAMES", url: "#games" },
                { text: "COLLECTIBLES", url: "#collectibles" },
                { text: "VIDEOS", url: "#videos" },
                { text: "FANS", url: "#fans" },
                { text: "NEWS", url: "#news" },
                { text: "SHOP", url: "#shop" },
            ],
            showMenu: false,
        };
    },
    methods: {
        toggleMenu() {
            this.showMenu = !this.showMenu;
        },
    },
};
</script>


<!-- HTML -->
<template>
    <header class="p-1">
        <div class="container row d-flex align-items-center">
            <div class="row">
                <div class="col-1">
                    <div class="img">
                        <img src="../assets/dc-logo.png" alt="">
                    </div>
                </div>
                <div class="col-3"></div>
                <div class="col-8 d-flex justify-content-end">
                    <button class="hamburger" @click="toggleMenu">
                        &#9776; <!-- Hamburger icon -->
                    </button>
                    <div class="nav" :class="{ 'active': showMenu }">
                        <a v-for="link in links" :href="link.url" @click="showMenu = false"><b>{{ link.text }}</b></a>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>


<!-- CSS -->
<style scoped>
header {
    height: 5.6rem;
}

nav {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 5.5rem;
}


.logo {
    margin-right: 15rem;
}

img {
    height: 5rem;
    width: 5rem;
    padding: 1rem;
}

a {
    padding: 1.8rem 1rem;
    font-size: 0.8rem;
    text-decoration: none;
    text-align: center;
    color: gray;
}

a:hover {
    border-bottom: 0.3rem solid rgb(2, 130, 249);
    background-color:rgb(2, 130, 249) ;
    color: rgb(255, 255, 255);
}

.row {
    display: flex;
    justify-content: center;
    margin: auto;
}

/* Hamburger menu styles */
.hamburger {
    display: none; /* Hidden by default */
    font-size: 2rem;
    background: none;
    border: none;
    cursor: pointer;
}

/* Responsive styles */
@media (max-width: 768px) {
    .nav {
        display: none; 
        flex-direction: column; 
        position: absolute;
        top: 5.6rem; 
        right: 0;
        background-color: white;
        width: 100%; 
        z-index: 1000; 
    }

    .nav.active {
        display: flex; 
    }

    .hamburger {
        display: block; 
        color: rgb(2, 130, 249);

    }

    a {
        padding: 1rem; 
        color: rgb(2, 130, 249);

    }
}
</style>