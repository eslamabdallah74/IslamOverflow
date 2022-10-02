<template>
    <section class="error-area section-padding position-relative">
        <span class="icon-shape icon-shape-1"></span>
        <span class="icon-shape icon-shape-2"></span>
        <span class="icon-shape icon-shape-3"></span>
        <span class="icon-shape icon-shape-4"></span>
        <span class="icon-shape icon-shape-5"></span>
        <span class="icon-shape icon-shape-6"></span>
        <span class="icon-shape icon-shape-7"></span>
        <div class="container">
            <div class="media align-items-center justify-content-center error-content">
                <img style="width: 400px;" src="/img/404.png" alt="error-image"
                    class="img-fluid mr-5 error-content-img">
                <div class="media-body flex-inherit">
                    <h2 class="section-title pb-3">الصفحة غير موجودة!</h2>
                    <p class="section-desc pb-4">معذرةً ، لم نتمكن من العثور على الصفحة التي طلبتها.</p>
                    <ul class="generic-list-item">
                        <li>تصفح <NuxtLink to="/Questions">أجدد الأسألة</NuxtLink>
                        </li>
                        <li> يمكنك أيضا أن <NuxtLink to="/Questions/Ask"> تسأل سؤلا</NuxtLink>
                        </li>
                        <li> لمزيد من الأستفسارات <NuxtLink to="/Questions"> نواصل معنا</NuxtLink>
                        </li>
                    </ul>
                </div>
            </div>
        </div><!-- end container -->
    </section>
</template>

<style scoped>
.generic-list-item li a {
    display: inline-block;
    color: #2d86eb !important;
}
</style>

<script setup>
const config = useRuntimeConfig();

useHead({
    title: "Not Found - " + config.APP_NAME
})
</script>