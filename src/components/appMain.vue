<script>
import dcCard from './_dcCard.vue'

export default {
    name: 'appMain',
    components: {
        dcCard
    },


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
            ],

            dcComics: [
                {
                    "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book",
                },
                {
                    "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book",
                },
                {
                    "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel",
                },
                {
                    "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book",
                },
                {
                    "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel",
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
              <dcCard v-for="dcComics, index in dcComics" :key="index" :dcComics="dcComics"/>
            </div>
        </div>

        <div class="container-celeste">
            <div class="contenuto-celeste">
                <ul>
                    <li v-for="(icone, index) in icone" :key="index" >
                        <div class="d-flex card-icone">
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

.card-icone {
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
    margin: 0 auto;
    display: flex;
    align-items: center;
    flex-wrap: wrap;
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