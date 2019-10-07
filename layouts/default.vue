<template>
    <div>
        <!-- Navigation -->
        <Navigation />
        <!-- Content -->
        <div class="container content">
            <nuxt/>
        </div>
        <!-- Footer -->
        <div class="footer">
            Copyright by me
        </div>
    </div>
</template>

<script>
import Navigation from "~/components/navigation"
import Banner from "~/components/banner.vue"

export default {
    components: {
        Navigation,
        Banner
    }
}
</script>