<script>
export default {
    name: 'appFooter',
    data() {
        return {
            comics: [
                {
                    titolo: "Characters"
                },
                {
                    titolo: "Comics"
                },
                {
                    titolo: "Movies"
                },
                {
                    titolo: "TV"
                },
                {
                    titolo: "Games"
                },
                {
                    titolo: "Videos"
                },
                {
                    titolo: "News"
                },
            ],

            shop: [
                {
                    titolo: "Shop DC"
                },
                {
                    titolo: "Shop DC Collectibles"
                }

            ],

            dc: [
                {
                    titolo: "Terms Of Use"
                },
                {
                    titolo: "Privacy policy(New)"
                },
                {
                    titolo: "Ad Choices"
                },
                {
                    titolo: "Advertising"
                },
                {
                    titolo: "Jobs"
                },
                {
                    titolo: "Subscriptions"
                },
                {
                    titolo: "Talent Workshops"
                },
                {
                    titolo: "CPSC Certificates"
                },
                {
                    titolo: "Ratings"
                },
                {
                    titolo: "Shop Help"
                },
                {
                    titolo: "Contact US"
                },
            ],

            sites: [
                {
                    titolo: "DC"
                },
                {
                    titolo: "MAD Magazine"
                },
                {
                    titolo: "DC Kids"
                },
                {
                    titolo: "DC Universe"
                },
                {
                    titolo: "JDC Power Visa"
                },
            ]
        }
    },
}
</script>

<template lang="">
    <footer>
        <div class="contenitore-ul">
            <div class="col-dc-comics">
                <h2 class="margin-top-40">DC COMICS</h2>
                <ul>
                    <li v-for="(comics, index) in comics" :key="index">
                        <div>{{comics.titolo}}</div>
                    </li>
                </ul>
    
                <h2 class="margin-top-20">Shop</h2>
                <ul>
                    <li v-for="(shop, index) in shop" :key="index">
                        <div>{{shop.titolo}}</div>
                    </li>
                </ul>
            </div>
            <div class="margin-left-40">
                <h2>DC</h2>
                <ul>
                    <li v-for="(dc, index) in dc" :key="index">
                        <div>{{dc.titolo}}</div>
                    </li>
                </ul>
            </div>

            <div class="margin-left-40">
                <h2>SITES</h2>
                <ul>
                    <li v-for="(sites, index) in sites" :key="index">
                        <div>{{sites.titolo}}</div>
                    </li>
                </ul>
            </div>
            <div class="img-logo"></div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
footer {
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    position: relative;

}



.contenitore-ul {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;

}

h2 {
    color: white;
}

ul {
    list-style-type: none;
    color: grey;
    margin-top: 10px;
    font-size: 20px;
}

li:hover {
    color: rgb(35, 146, 250)
}

li {
    margin-top: 5px;
    cursor: pointer;
}

.col-dc-comics {
    width: 250px;
}

.margin-top-40 {
    margin-top: 40px;
}

.margin-top-20 {
    margin-top: 20px;
}


.margin-left-40 {
    margin-top: 40px;
    margin-left: 40px;
    margin-bottom: 50px;
}

.img-logo {
    background-image: url("../assets/img/dc-logo-bg.png");
    width: 100%;
    height: auto;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    margin-left: 50px;
}
</style>