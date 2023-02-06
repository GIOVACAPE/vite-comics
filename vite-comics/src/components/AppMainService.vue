<script>
export default {
    name: 'AppMainService',
    data() {
        return {
            serviceList: [ // Service Items
                {
                    imgUrl: 'buy-comics-digital-comics.png',
                    text: 'Digital Comics'
                },
                {
                    imgUrl: 'buy-comics-merchandise.png',
                    text: 'DC Merchandise'
                },
                {
                    imgUrl: 'buy-comics-subscriptions.png',
                    text: 'Subscription'
                },
                {
                    imgUrl: 'buy-comics-shop-locator.png',
                    text: 'Comic Shop Locator'
                },
                {
                    imgUrl: 'buy-dc-power-visa.svg',
                    text: 'DC Power Visa'
                },
            ]
        }
    },

    methods: {
        //Find img on directory (Absolute path)
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
}
</script>

<template>
    <section id="service">
        <div class="service-cards d-flex container-wrapped">

            <div v-for="serviceItem in serviceList" class="single-card d-flex align-center">
                <img :src="getImagePath(`../assets/${serviceItem.imgUrl}`)" :alt="serviceItem.text">
                <h2>{{ serviceItem.text }}</h2>
            </div>

        </div>
    </section>
</template>

<style lang="scss">
@use '../styles/partials/variables.scss' as *;

section#service {
    background-color: $brand-color;
    padding: 2rem 0;
}

div.single-card {
    width: calc((100% / 5) - 1rem);
    padding: 0 .5rem;
    justify-content: center;

    img {
        width: 55px;
        height: 55px;
        object-fit: contain;
        margin-right: .5rem;
    }

    h2 {
        font-size: 1rem;
        color: $white;
        text-transform: uppercase;
        font-weight: 300;
    }
}
</style>