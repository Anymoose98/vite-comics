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
                    img: "../assets/img/buy-comics-digital-comics.png",
                    titolo: "DC POWER VISA"
                },
            ]
        }
    },
}
</script>

<template lang="">
    <main>
        <div class="container-nero">
            <div class="contenuto-nero">
                <h1> --> Content goes here <-- </h1>
            </div>
        </div>

        <div class="container-celeste">
            <div class="contenuto-celeste">
                <ul>
                    <li v-for="(icone, index) in icone" :key="index">
                        <div class="d-flex">
                            <img src= "../assets/img/buy-comics-digital-comics.png" :alt="icone.titolo">
                            <div class="white">{{ icone.titolo }}</div>
                        </div>
                    </li>
                    
                </ul>
            </div>
        </div>
    </main>
</template>


<style lang="scss" scoped>
.d-flex {
    height: 100%;
    display: flex;
    align-items: center;


}

.white {
    color: white;
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
    height: 150px;
    margin: 0 auto;
    display: flex;
    align-items: center
}

h1 {
    color: white;
}
</style>