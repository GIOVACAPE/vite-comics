<script>
export default {
    name: 'FooterBottom',
}
</script>

<template>
    <section id="bottom-footer">
        <div class="container-wrapped d-flex flex-between">
            <a href="#" class="btn">Sign-Up Now!</a>
            <div class="social-btn d-flex align-center">
                <h3>Follow Us</h3>
                <ul>
                    <li>
                        <a href="#"><img src="../../assets/footer-facebook.png" alt=""></a>
                    </li>
                    <li>
                        <a href="#"><img src="../../assets/footer-twitter.png" alt=""></a>
                    </li>
                    <li>
                        <a href="#"><img src="../../assets/footer-youtube.png" alt=""></a>
                    </li>
                    <li>
                        <a href="#"><img src="../../assets/footer-pinterest.png" alt=""></a>
                    </li>
                    <li>
                        <a href="#"><img src="../../assets/footer-periscope.png" alt=""></a>
                    </li>
                </ul>
            </div>
        </div>
    </section>
</template>


<style lang="scss" scoped>
@use '../../styles/partials/variables.scss' as *;


section#bottom-footer {
    background-color: $footer-bg;
    padding: 2rem;
}

a.btn {
    font-size: 1.2rem;
    text-decoration: none;
    color: $white;
    text-transform: uppercase;
    padding: 1rem 2rem;
    border: 2px solid $brand-color;

    &:hover {
        color: $brand-color;
        background-color: $white;
    }
}



div.social-btn {
    h3 {
        color: $brand-color;
        text-transform: uppercase;
        font-size: 1.5rem;
        margin-right: 1rem;
        font-weight: bold;
    }

    ul {
        display: flex;

        li {
            list-style-type: none;
            padding: 0 .7rem;

            a img {
                transform: scale(1.2);
                vertical-align: middle;

                &:hover {
                    transition: all .2s ease-in-out;
                    transform: scale(1);
                }
            }
        }
    }
}
</style>