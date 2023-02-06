<script>
export default {
    name: 'FooterTop',
    data() {
        return {
            // Arrays OBj for footer nav
            docComicsItems: [
                {
                    text: 'Characters',
                    url: '#'
                },
                {
                    text: 'Comics',
                    url: '#'
                },
                {
                    text: 'Movies',
                    url: '#'
                },
                {
                    text: 'TV',
                    url: '#'
                },
                {
                    text: 'Games',
                    url: '#'
                },
                {
                    text: 'Videos',
                    url: '#'
                },
                {
                    text: 'News',
                    url: '#'
                },
            ],

            shopItems: [
                {
                    text: 'Shop DC',
                    url: '#'
                },
                {
                    text: 'Shop DC Collectibles',
                    url: '#'
                },
            ],

            DCItems: [
                {
                    text: 'Term Of Use',
                    url: '#'
                },
                {
                    text: 'Privacy policy (New)',
                    url: '#'
                },
                {
                    text: 'Ad Choices',
                    url: '#'
                },
                {
                    text: 'Advertising',
                    url: '#'
                },
                {
                    text: 'Jobs',
                    url: '#'
                },
                {
                    text: 'Subscriptions',
                    url: '#'
                },
                {
                    text: 'Talent Workshop',
                    url: '#'
                },
                {
                    text: 'CPSC Certificates',
                    url: '#'
                },
                {
                    text: 'Rating',
                    url: '#'
                },
                {
                    text: 'Shop Help',
                    url: '#'
                },
                {
                    text: 'Contact US',
                    url: '#'
                },
            ],

            siteItems: [
                {
                    text: 'DC',
                    url: '#'
                },
                {
                    text: 'MAD Magazine',
                    url: '#'
                },
                {
                    text: 'DC Kids',
                    url: '#'
                },
                {
                    text: 'DC Universe',
                    url: '#'
                },
                {
                    text: 'DC Power Visa',
                    url: '#'
                },
            ]
        }
    }
}
</script>

<template>
    <section id="top-footer">
        <div class="container-wrapped d-flex flex-between">
            <div class="nav-info d-flex">

                <nav class="d-flex">
                    <div class="nav-wrap">
                        <div class="single-nav">
                            <h2>DC Comics</h2>
                            <!-- Generate Nav for DC Comics  -->
                            <ul>
                                <li v-for="item in docComicsItems">
                                    <a :href="item.url">{{ item.text }}</a>
                                </li>
                            </ul>
                        </div>

                        <div class="single-nav shop-nav">
                            <h2>Shop</h2>
                            <!-- Generate Nav for Shop  -->

                            <ul>
                                <li v-for="item in shopItems">
                                    <a :href="item.url">{{ item.text }}</a>
                                </li>
                            </ul>
                        </div>
                    </div>

                    <div class="single-nav">
                        <h2>DC</h2>
                        <!-- Generate Nav for DC  -->

                        <ul>
                            <li v-for="item in DCItems">
                                <a :href="item.url">{{ item.text }}</a>
                            </li>

                        </ul>
                    </div>

                    <div class="single-nav">
                        <h2>Sites</h2>
                        <!-- Generate Nav for Sistes  -->
                        <ul>
                            <li v-for="item in siteItems">
                                <a :href="item.url">{{ item.text }}</a>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>

            <!-- DC Trasparent Logo  -->
            <div class="dc-bg-img">
                <img src="../../assets/dc-logo-bg.png" alt="Dc Bg Logo">
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use '../../styles/partials/variables' as *;

section#top-footer {
    background-image: url(../../assets/footer-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
}

div.nav-info {
    padding: 2rem 0;
}

div.single-nav {
    margin-right: 2rem;
    width: max-content;

    h2 {
        font-weight: bold;
        font-size: 1.5rem;
        margin-bottom: .5rem;
        color: $white;
        text-transform: uppercase;
    }

    ul li {
        list-style-type: none;
        margin: .15rem 0;

        a {
            text-decoration: none;
            color: $white;
            font-weight: 300;
            font-size: .8rem;
            filter: opacity(.6);

            &:hover {
                filter: opacity(1);
            }
        }
    }

}

div.shop-nav {
    margin-top: 1.5rem;
}

div.nav-info nav {
    padding: 0 1rem;
}

div.dc-bg-img {
    width: 100%;
    position: relative;
    overflow: hidden;

    img {
        height: 150%;
        position: absolute;
        top: 50%;
        right: 0;
        transform: translateY(-50%);
    }
}
</style>