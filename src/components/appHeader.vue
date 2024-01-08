<script>
export default {
    name: 'appHeader',
    data() {
        return {
            menu: [
                {
                    label: 'CHARACTERS'
                },
                {
                    label: 'COMICS'
                },
                {
                    label: 'MOVIES'
                },
                {
                    label: 'TV'
                },
                {
                    label: 'GAMES'
                },
                {
                    label: 'COLLECTIBLES'
                },
                {
                    label: 'VIDEOS'
                },
                {
                    label: 'FANS'
                },
                {
                    label: 'NEWS'
                },
                {
                    label: 'SHOP'
                },
            ]
        }
    }
}
</script>

<template lang="">
    <header>
        <div class="col">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div>
            <nav>
                <ul>
                    <li v-for="(label, index) in menu" :key="index" >
                        <a href="">{{menu[index].label}}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>


<style lang="scss" scoped>
header {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    margin-top: 10px;
    margin-bottom: 10px;
}

ul {
    list-style-type: none;
}

li {
    display: inline-block;
    margin: 10px;
    font-weight: bold;
    font-size: small;
}

a {
    text-decoration: none;
    color: black;
}

a:hover {
    color: rgb(35, 146, 250)
}

.col {
    width: 30%;
}

nav {
    height: 100%;
    display: flex;
    align-items: center
}
</style>