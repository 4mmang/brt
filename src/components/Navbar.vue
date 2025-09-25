<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isMenuOpen = ref(false)
const isFixed = ref(false)

function toggleMenu() {
    isMenuOpen.value = !isMenuOpen.value
}

function handleScroll() {
    isFixed.value = window.scrollY > 0
}

// smooth scroll dengan offset navbar
function scrollToSection(e: Event, id: string) {
    e.preventDefault()
    const target = document.querySelector(id)
    if (target) {
        const navbarHeight = 120 // sesuaikan dengan tinggi header
        const top = (target as HTMLElement).offsetTop - navbarHeight
        window.scrollTo({
            top,
            behavior: 'smooth',
        })
        isMenuOpen.value = false // auto close menu mobile
    }
}

onMounted(() => {
    window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
    <header :class="[
        'bg-transparent absolute top-0 left-0 w-full flex items-center z-10 transition',
        { 'navbar-fixed': isFixed }
    ]">
        <div class="container flex justify-between items-center relative">
            <!-- Logo -->
            <div class="px-5">
                <a href="#home" @click="scrollToSection($event, '#home')"
                    class="font-bold text-3xl flex items-center py-6">
                    <img src="/brt.png" class="mr-3" width="70" height="70" alt="" />
                    <span class="text-4xl text-primary hidden md:block lg:block">
                        Bandar Room Tech
                    </span>
                </a>
            </div>

            <!-- Menu -->
            <div class="flex items-center px-4">
                <button id="hamburger" type="button" @click="toggleMenu" class="block absolute right-7 lg:hidden"
                    :class="{ 'hamburger-active': isMenuOpen }">
                    <span class="hamburger-line transition duration-300 ease-in-out origin-top-left" />
                    <span class="hamburger-line transition duration-300 ease-in-out" />
                    <span class="hamburger-line transition duration-300 ease-in-out origin-top-left" />
                </button>

                <nav id="nav-menu" :class="[
                    'absolute py-5 bg-white shadow-lg rounded-lg max-w-[250px] w-full right-4 top-full lg:block lg:static lg:bg-transparent lg:max-w-full lg:shadow-none lg:rounded-none',
                    { hidden: !isMenuOpen }
                ]">
                    <ul class="block lg:flex">
                        <li class="group">
                            <a href="#home" @click="scrollToSection($event, '#home')"
                                class="text-base text-primary py-2 mx-8 flex">
                                Home
                            </a>
                        </li>
                        <li class="group">
                            <a href="#about" @click="scrollToSection($event, '#about')"
                                class="text-base text-primary py-2 mx-8 flex">
                                About Us
                            </a>
                        </li>
                        <li class="group">
                            <a href="#services" @click="scrollToSection($event, '#services')"
                                class="text-base text-primary py-2 mx-8 flex">
                                Services
                            </a>
                        </li>
                        <li class="group">
                            <a href="#portofolio" @click="scrollToSection($event, '#portofolio')"
                                class="text-base text-primary py-2 mx-8 flex">
                                Portofolio
                            </a>
                        </li>
                        <li class="group">
                            <a href="#team" @click="scrollToSection($event, '#team')"
                                class="text-base text-primary py-2 mx-8 flex">
                                Training
                            </a>
                        </li>
                        <!--
            <li class="group">
              <a
                id="contact-me"
                href="#contact"
                @click="scrollToSection($event, '#contact')"
                class="text-base bg-primary text-white py-2 px-4 rounded-full mx-8 flex"
              >
                Contact Us
              </a>
            </li>
            -->
                    </ul>
                </nav>
            </div>
        </div>
    </header>
</template>
