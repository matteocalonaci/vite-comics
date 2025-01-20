<script>
export default {
    name: "AppFooter",
    data() {
        return {
            cards: [
                {
                    text: "DIGITAL COMICS",
                    percorso: "./src/assets/buy-comics-digital-comics.png",
                },
                {
                    text: "DC MERCHANDISE",
                    percorso: "./src/assets/buy-comics-merchandise.png",
                },
                {
                    text: "SUBSCRIPTION",
                    percorso: "./src/assets/buy-comics-subscriptions.png",
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    percorso: "./src/assets/buy-comics-shop-locator.png",
                },
                {
                    text: "DC POWER VISA",
                    percorso: "./src/assets/buy-dc-power-visa.svg",
                },
            ],

            images: [
                {
                    src: "./src/assets/footer-facebook.png",
                },
                {
                    src: "./src/assets/footer-twitter.png",
                },
                {
                    src: "./src/assets/footer-youtube.png",
                },
                {
                    src: "./src/assets/footer-pinterest.png",
                },
                {
                    src: "./src/assets/footer-periscope.png",
                },
            ],

            comicsLinks: [`Characters`, `Comics`, `Movies`, `Tv`, `Games`, `Videos`, `News`],
            shopLinks: [`Shop DC`, `Shop DC Collectibles`],
            dcLinks: [
                `Terms Of Use`,
                `Privacy policy (New)`,
                `Ad Choices`,
                `Advertising`,
                `Jobs`,
                `Subscriptions`,
                `Talent Workshops`,
                `CPSC Certificates`,
                `Ratings`,
                `Shop Help`,
                `Contact Us`,
            ],
            sitesLinks: [`DC`, `MAD Magazine`, `DC Kids`, `DC Universe`, `DC Power Vista`],
        }
    },

    methods: {

    },

    mounted() {

    }
}
</script>
<template>
    <footer>
        <!-- FASCIONE AZZURRO -->
        <div class="frst-section">
            <div class="row p-3">
                <div class="col-6 col-md-4 col-lg-2" v-for="card in cards" :key="card.text">
                    <div class="row align-items-center">
                        <div class="img col-4">
                            <img :src="card.percorso" alt="">
                        </div>
                        <div id="text" class="col-8 text-white">{{ card.text }}</div>
                    </div>
                </div>
            </div>
        </div>

        <!-- LINK VARI -->
        <div class="scnd-section">
            <div class="container">
                <div class="row">
                    <!-- PARTE SX -->
                    <div class="col-12 col-md-6 p-2">
                        <div class="row">
                            <div class="col-6 col-md-4">
                                <span class="fs-6 fw-bold">DC COMICS</span>
                                <ul class="p-0 mt-2">
                                    <li v-for="link in comicsLinks" class="list-group-item text-white-50 lh-base">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                                <span class="fs-6 fw-bold">SHOP</span>
                                <ul class="p-0 mt-2">
                                    <li v-for="link in shopLinks" class="list-group-item text-white-50 lh-base">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>
                            <div class="col-6 col-md-4">
                                <span class="fs-6 fw-bold">DC</span>
                                <ul class="p-0 mt-2">
                                    <li v-for="link in dcLinks" class="list-group-item text-white-50 lh-base">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>
                            <div class="col-6 col-md-4">
                                <span class="fs-6 fw-bold">SITES</span>
                                <ul class="p-0 mt-2">
                                    <li v-for="link in sitesLinks" class="list-group-item text-white-50 lh-base">
                                        <a href="#">{{ link }}</a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!-- PARTE DX -->
                    <div id="main-footer-dx" class="col-12 col-md-6 text-center">
                        <img class="img-footer" src="../assets/dc-logo-bg.png" alt="">
                    </div>
                </div>
            </div>
        </div>

        <!-- BTN + FOLLOW-US -->
        <div class="thrd-section py-3">
            <div class="container row m-auto justify-content-between align-items-center">
                <div class="col-12 col-md-2 text-center">
                    <button type="button" class="btn">SIGN-UP NOW!</button>
                </div>
                <div class="col-12 col-md-8 txt-end">
                    <span class="f-us"><b>FOLLOW US</b></span>
                    <div class="d-flex justify-content-end">
                        <img id="icons" :src="img.src" alt="" v-for="img in images" class="me-2">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<!-- CSS -->
<style scoped>
.frst-section {
    position: sticky;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 8rem;
    background-color: rgb(2, 130, 249);
    padding: 1rem;
}

.row {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: auto;
}

img {
    width: 100%;
}

#text {
    font-size: 0.8rem;
    padding-left: 1rem;
    color: white;
}

/* SEZIONE CON LINK VARI */
.scnd-section {
    background-image: url(../assets/footer-bg.jpg);
    background-size: cover;
    padding: 2rem 0;
}

#main-footer-dx {
    height: 20rem;
    position: relative;
}

.img-footer {
    width: 65%;
    position: absolute;
    bottom: -2rem;
    right: 1rem;
}

/* SEZIONE BUTTON + FOLLOW US */
.thrd-section {
    background-color: #484848;
    padding: 1rem;
}

#icons {
    width: 2rem;
    margin: 1rem;
}

.btn {
    border: 0.2rem solid rgb(2, 130, 249);
    color: white;
    font-size: 1rem;
    padding: 0.5rem 2rem;
    width: auto;
}

.txt-end {
    text-align: end;
}

.f-us {
    color: rgb(2, 130, 249);
}

.inizio {
    padding-bottom: 9rem;
}

a {
    padding: 1rem 0.5rem;
    font-size: 0.9rem;
    text-decoration: none;
    color: gray;
}


@media (max-width: 480px) {
    #text {
        font-size: 0.7rem; /* Slightly larger font size for better readability */
        padding-left: 0; /* Remove padding for a cleaner look */
        margin-top: 0.5rem; /* Add some margin for spacing */
    }

    .frst-section {
        height: auto; /* Allow height to adjust based on content */
        padding: 0.5rem 0; /* Add some padding for spacing */
    }

    .scnd-section {
        height: auto; /* Allow height to adjust based on content */
        padding: 1rem; /* Maintain padding for spacing */
    }
    

    .btn {
        font-size: 0.9rem; /* Keep button font size reasonable */
        padding: 0.5rem; /* Adjust padding for a better fit */
        width: 100%; /* Full width button for easier tapping */
    }

    .img-footer {
    position: absolute;
    bottom: auto;
    right: 0.5rem;
}

    #icons {
        width: 1.5rem; /* Maintain icon size */
        margin: 0.5rem; /* Add margin for spacing */
    }

    .f-us {
        font-size: 0.9rem; /* Keep font size reasonable */
        text-align: center; /* Center align text */
        display: block; /* Ensure it takes full width */
        margin-top: 0.5rem; /* Add margin for spacing */
    }
}
</style>