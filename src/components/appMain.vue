<script>
export default {

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

            </div>
        </div>
    </main>
</template>


<style lang="scss" scoped>
* {
    margin: 0;
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