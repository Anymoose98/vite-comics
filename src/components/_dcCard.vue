<script>
export default {
    name: 'dcCard',
    props: {
        dcComics: Object
    },
    methods: {
        getImagePath: function (img) {
            return new URL(img, import.meta.url).href;
        }
    }
};

</script>

<template lang="">
        <div class="card">
            <img :src="getImagePath(dcComics.thumb)"  class="img-card">
            <h4>{{dcComics.series}}</h4>
        </div>
</template>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 30px);
    margin: 15px;
    margin-top: 30px;
    height: 250px;
    margin-bottom: 50px;
}

.img-card {
    width: 100%;
    height: 200px;
    position: relative;
}

h4 {
    color: white;
    text-transform: uppercase;
    text-align: center;
}
</style>