<script setup lang="ts">
import { Code, Terminal } from 'lucide-vue-next'
</script>
<template>
    <!-- About Section Start -->
    <section id="services" class="pt-18 pb-18 scroll-mt-30">
        <div class="container">
            <div class="flex flex-wrap">
                <div class="w-full px-4 lg:px-4 mb-10 lg:w-1/3">
                    <h4 class="font-bold uppercase text-3xl mb-3">Our Services</h4>
                </div>

                <div class="w-full px-4 lg:px-0 lg:w-2/3">
                    <h3 class="text-2xl mb-8 lg:text-4xl">We help you grow coding skills and build digital
                        products.</h3>
                    <div class="grid grid-cols-1 gap-4 lg:grid-cols-2 lg:gap-8">
                        <div
                            class="h-42 flex flex-col justify-center items-center rounded-2xl bg-primary text-white shadow-2xl">
                            <p class="text-2xl tracking-wide font-bold">Software Development</p>
                            <Code class="w-20 h-20" />
                        </div>

                        <div class="h-42 flex flex-col justify-center items-center rounded-2xl bg-primary text-white shadow-2xl">
                            <p class="text-2xl tracking-wide font-bold">Training Programming</p>
                            <Terminal class="w-20 h-20" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    <!-- About Section End -->
</template>