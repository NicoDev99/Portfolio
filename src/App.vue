<template>
    <div class="bg-[url('./img/fond.png')] w-full h-screen bg-cover pt-10 relative">

        <!-- Computer screen nav menu -->
        <nav class="border-y borer-solid border-[#767478] mx-auto w-5/6 py-3 max-w-5xl hidden lg:flex items-center justify-center">
            <Logo width="30" height="30" class="mr-12"/>
            <ul class="flex gap-x-10">
                <CompNavLink name="Accueil" link="/" number="01" />
                <CompNavLink name="Présentation" link="#about-me" number="02" />
                <CompNavLink name="Compétences" link="#skills" number="03" />
                <CompNavLink name="Mes projets" link="#my-projects" number="04" />
                <CompNavLink name="Contact" link="#contact" number="05" />
            </ul>
        </nav>

        <!-- Phone screen nav menu -->
        <div class="block lg:hidden">
            <div class="flex justify-between items-center mx-12">
                <BurgerIcon width="40" height="40" color="white" class="cursor-pointer" @click="this.togglePhoneNav()"/>
                <Logo width="40" height="40"/>
            </div>
            <nav class="bg-[#151A1E] w-full h-screen absolute top-0 transition ease duration-300 z-10" :class="!this.isPhoneNavDisplay ? '-translate-y-full' : '-translate-y-0'">
                <CloseIcon width="40" height="40" color="white" class="cursor-pointer mt-12 ml-10" @click="this.togglePhoneNav()" />
                <ul class="text-center mt-20">
                    <Logo height="60" width="60" class="block w-16 mx-auto mb-16"/>
                    <PhoneNavLink name="Accueil" link="/" />
                    <PhoneNavLink name="Présentation" link="#about-me" />
                    <PhoneNavLink name="Compétences" link="#skills" />
                    <PhoneNavLink name="Mes projets" link="#my-projects" />
                    <PhoneNavLink name="Contact" link="#contact" />
                </ul>
            </nav>
        </div>

        <div class="block text-center">
            <ArrowIcon color="white" class="block m-auto mt-24 animate-bounce" />

            <TitleSide class="mt-16">
                <h1 class="font-Habibi text-white text-2xl sm:text-4xl uppercase translate-y-6 animate-[transformBottomTop_1s_ease_forwards]">Erwan Nicolas</h1>
            </TitleSide>

            <h2 class="text-white font-Gruppo mt-6 text-xl sm:text-3xl translate-y-6 animate-[transformBottomTop_1s_ease_forwards]">Développeur Web Full-Stack</h2>

            <Separator class="block mx-auto mt-12 translate-y-6 animate-[transformBottomTop_1s_ease_forwards]"/>
        </div>

        <div class="absolute bottom-10 left-1/2 -translate-x-1/2 cursor-pointer border border-solid border-white rounded-full px-1 py-2.5">
            <a href="#about-me">
                <ArrowIcon color="white" class="block m-auto animate-[transformTopBottom_1s_ease]" />
            </a>
        </div>
    </div>
</template>


<script>
    import BurgerIcon from './components/icons/Burger.vue'
    import CompNavLink from "./components/ComputerNavLink.vue"
    import PhoneNavLink from "./components/PhoneNavLink.vue"
    import CloseIcon from "./components/icons/Close.vue"
    import Logo from "./components/icons/Logo.vue";
    import ArrowIcon from "./components/icons/Arrow.vue"
    import Separator from "./components/Separator.vue"
    import TitleSide from "./components/TitleSide.vue"

    export default {
        components: {
            CompNavLink,
            BurgerIcon,
            PhoneNavLink,
            CloseIcon,
            Logo,
            ArrowIcon,
            Separator,
            TitleSide
        },

        data() {
            return {
                isPhoneNavDisplay: false,
            }
        },

        methods: {
            
            /**
             * Switch the phone menu (hidden to visible and inversly)
             * 
             * @return {void}
             */
            togglePhoneNav : function() {
                this.isPhoneNavDisplay = !this.isPhoneNavDisplay
            }
        }
    }
</script>
