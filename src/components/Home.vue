<script setup lang="ts">
defineProps<{}>()
</script>
<template>
    <!-- Hero Section Start -->
    <section id="home" class="pt-36 pb-18 lg:pb-32">
        <div class="container">
            <div class="flex flex-wrap lg:flex-nowrap">
                <!-- Text Column -->
                <div class="w-full self-center px-8 lg:px-12 xl:px-12 md:px-12 lg:w-1/2">
                    <p class="font-semibold text-primary text-3xl lg:hidden lg:text-8xl">
                        Welcome to Bandar Room Tech
                    </p>
                    <h1 class="font-semibold text-primary hidden lg:block mb-5 mt-12 text-2xl lg:text-4xl">
                        Hello friend 👋, welcome
                    </h1>
                    <h2 class="font-medium text-slate-500 text-lg mb-5 lg:hidden lg:text-xl">
                        Technology Solution
                    </h2>
                    <p class="font-medium text-secondary text-xl mb-10 leading-relaxed">
                        <span class="font-bold text-primary">Bandar Room Tech</span> is a platform that offers software development services and programming training, designed to
                        help individuals and businesses grow their tech skills and create impactful solutions
                    </p>
                    <a href="https://wa.me/6282290762799" id="contact-me"
                        class="text-base font-semibold text-white bg-primary py-3 px-8 rounded-full hover:bg-blue-400 transition duration-300 ease-in-out">
                        Contact Us
                    </a>
                </div>

                <!-- Image Column -->
                <div class="w-full self-end px-4 lg:w-1/2 mt-14 lg:mt-7">
                    <div class="relative lg:mt-8 lg:right-0">
                        <img src="https://images.unsplash.com/photo-1502685104226-ee32379fefbe?w=400" alt="Arman Umar"
                            class="max-w-full mx-auto" />
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- Hero Section End -->
</template>