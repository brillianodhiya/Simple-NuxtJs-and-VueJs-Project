<template>
    <div>
        <div v-swiper:mySwiper="swiperOption">
            <div class="swiper-wrapper">
                <div class="swiper-slide" v-for="item in banner" v-bind:key="item.key">
                    <img :src="item.src" alt="item.src">
                </div>
            </div>
            <div class="swiper-pagination" slot="pagination"></div>
        </div>
    </div>
</template>

<script>
export default {
    data () {
        return {
            banner: [{
                src: 'https://dummyimage.com/800x400/206de0/ffffff'
            }, {
                src: 'https://dummyimage.com/800x400/206de0/ffffff'
            }, {
                src: 'https://dummyimage.com/800x400/206de0/ffffff'
            }, {
                src: 'https://dummyimage.com/800x400/206de0/ffffff'
            }, {
                src: 'https://dummyimage.com/800x400/206de0/ffffff'
            }, {
                src: 'https://dummyimage.com/800x400/206de0/ffffff'
            }],
            swiperOption: {
                slidesPerView: 1,
                spaceBetween: 8,
                breakpoints: {
                    320: {
                        slidesPerView: 1,
                        spaceBetween: 8
                    },
                    400: {
                        slidesPerView: 2,
                        spaceBetween: 8
                    },
                    800: {
                        slidesPerView: 3,
                        spaceBetween: 8
                    }
                },
                autoplay: {
                    delay: 5000,
                    disableOnInteraction: false
                },
                pagination: {
                    el: '.swiper-pagination'
                }
            }
        }
    }
}
</script>