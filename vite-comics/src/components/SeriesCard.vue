<script>
export default {
    name: 'SeriesCard',
    // Import Props
    props: [
        'srThumb', 'srPrice', 'srSeries', 'srType'
    ]
}
</script>

<template>
    <article class="series-card">
        <div class="thum-container">
            <div class="hover-thumb d-flex">
                <div class="hover-content">
                    <span>{{ srPrice }}</span>
                    <span class="type-card">{{ srType }} </span>
                </div>
            </div>
            <img :src="srThumb" :alt="srSeries">
        </div>
        <h4>{{ srSeries }}</h4>
    </article>
</template>


<style lang="scss">
@use '../styles/partials/variables' as *;

article {
    width: calc((100% / 6) - 1rem);
    margin: 1rem .5rem;
    overflow: hidden;


    div.thum-container {
        width: 220px;
        height: 220px;
        overflow: hidden;
        margin-bottom: 1.2rem;
        position: relative;

        img {
            display: block;
            width: 100%;
        }

        div.hover-thumb {
            position: absolute;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.719);
            cursor: pointer;
            display: none;

            div.hover-content {
                margin: auto;

                span {
                    text-align: center;
                    display: block;
                    text-transform: uppercase;
                    margin: .5rem 0;

                }

                .type-card {
                    color: $brand-color;
                    font-weight: 700;
                }
            }

        }

        &:hover div.hover-thumb {
            display: flex;
        }
    }

    h4 {
        text-transform: uppercase;
        margin-bottom: .8rem;
        font-weight: 200;
    }



}
</style>