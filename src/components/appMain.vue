<script>
export default {
    name: 'appMain',
    data() {
        return {
            icone: [
                {
                    img: "../assets/img/buy-comics-digital-comics.png",
                    titolo: "DIGITAL COMICS"
                },
                {
                    img: "../assets/img/buy-comics-merchandise.png",
                    titolo: "DC MERCHANDISE"
                },
                {
                    img: "../assets/img/buy-comics-subscriptions.png",
                    titolo: "SUBSCRIPTION"
                },
                {
                    img: "../assets/img/buy-comics-shop-locator.png",
                    titolo: "COMIC SHOP LOCATOR"
                },
                {
                    img: "../assets/img/buy-dc-power-visa.svg",
                    titolo: "DC POWER VISA"
                },
            ]
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL(img, import.meta.url).href;
        }
    }
}
</script>

<template lang="">
    <main>

        <div class="sfondo-img"></div>

        <div class="container-nero">
            <div class="contenuto-nero">
                <h1> --> Content goes here <-- </h1>
            </div>
        </div>

        <div class="container-celeste">
            <div class="contenuto-celeste">
                <ul>
                    <li v-for="(icone, index) in icone" :key="index" >
                        <div class="d-flex card">
                            <img :src="getImagePath(icone.img)" :alt="icone.titolo" class="icone">
                            <div class="white">{{ icone.titolo }}</div>
                        </div>
                    </li>
                    
                </ul>
            </div>
        </div>
    </main>
</template>


<style lang="scss" scoped>
.sfondo-img {
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    width: 100%;
    height: 300px;
}

.d-flex {
    height: 100%;
    display: flex;
    align-items: center;
}

.card {
    width: calc(100% / 5);
}

.icone {
    height: 50px;
    width: 100%;
}


.white {
    color: white;
    cursor: pointer;
    width: 100%;
}

.white:hover {
    border-bottom: 2px solid rgb(0, 0, 0);
    /* Aggiunge una linea blu sotto il link al passaggio del mouse */
}

img {
    width: 50px;
    height: auto;
    margin-right: 10px;
}

li {
    margin-right: 10px;
    margin-left: 10px;
    display: inline-block;
}

ul {
    list-style-type: none;
    width: 100%;
}

.container-nero {
    background-color: black;
    width: 100%;
    margin: 0;
}

.contenuto-nero {
    max-width: 1200px;
    height: 150px;
    margin: 0 auto;
    display: flex;
    align-items: center
}

.container-celeste {
    background-color: rgb(35, 146, 250);
    width: 100%;
    margin: 0;
}

.contenuto-celeste {
    max-width: 1200px;
    padding-top: 30px;
    padding-bottom: 30px;
    margin: 0 auto;
    display: flex;
    align-items: center
}

h1 {
    color: white;
}
</style>