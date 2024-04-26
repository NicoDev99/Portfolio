<template>
    <div class="bg-[url('./img/fond.png')] bg-fixed w-full min-h-screen h-fit bg-cover pt-10 relative">

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
        <div class="block lg:hidden overflow-hidden">
            <div class="flex justify-between items-center mx-12">
                <BurgerIcon width="40" height="40" color="white" class="cursor-pointer" @click="this.togglePhoneNav()"/>
                <Logo width="40" height="40"/>
            </div>
            <nav class="bg-[#151A1E] w-full absolute top-0 transition ease duration-300 z-10" :class="!this.isPhoneNavDisplay ? '-translate-y-full' : '-translate-y-0 min-h-screen h-fit'">
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

        <div class="block text-center pb-44">
            <ArrowIcon color="white" class="block m-auto mt-24 animate-bounce" />

            <TitleSide class="mt-16">
                <h1 class="font-Habibi text-white text-2xl sm:text-4xl uppercase translate-y-6 animate-[transformBottomTop_1s_ease_forwards]">Erwan Nicolas</h1>
            </TitleSide>

            <h2 class="text-white font-Gruppo mt-6 text-xl sm:text-3xl translate-y-6 animate-[transformBottomTop_1s_ease_forwards]">Développeur Web Full-Stack</h2>

            <Separator class="block mx-auto mt-12 translate-y-6 animate-[transformBottomTop_1s_ease_forwards]"/>
        </div>

        <a href="#about-me" class="block mx-auto absolute bottom-6 left-0 right-0 cursor-pointer border border-solid border-white rounded-full w-fit">
            <ArrowIcon color="white" class="animate-[transformTopBottom_1s_ease] my-1.5 px-1 sm:px-0 sm:mx-1 sm:my-2.5" />
        </a>
    </div>


    <!-- Bg linear gradient -->
    <div class="bg-gradient-to-b from-[#161B1F] to-[#010204] w-full h-auto" :class="this.isPhoneNavDisplay ? 'hidden' : 'block'">
        
        <!-- About me -->
        <div class="pt-20 px-20">
            <div class="flex justify-between">
                <h1 class="uppercase font-ZenTokyoZoo text-8xl text-white leading-tight">A propos <br />de moi</h1>
                <img src="/img/shooting_star.png" alt="Etoile filante" class="w-1/3 h-[100px]">
            </div>

            <div class="relative pb-96 mx-32">
                <div class="flex gap-x-7 absolute -top-10">
                    <img src="/img/photo_profil.png" alt="Etoile filante" class="w-96 h-96 rounded-xl">

                    <div>
                        <h1 class="font-ZenOldMincho text-6xl text-white">Erwan Nicolas</h1>
                        <h2 class="text-white font-Gruppo mt-3 text-2xl">Développeur Web Full-Stack</h2>

                        <p class="font-Roboto text-white text-justify text-sm mt-7">
                            Etudiant en alternance en BUT Informatique à l'Université Côte d'Azur, je me distingue par ma passion polyvalente pour le développement, les nouvelles technologies, l'entrepreneuriat et la gendarmerie.<br /><br />
                            Actuellement engagé dans le prestigieux programme PEPITE, je façonne mon parcours au sein de la formation D2E, où j'approfondis mes connaissances en matière d'entrepreneuriat. Mon expertise s'étend du développement informatique à la création de business plans, de l'interaction avec les investisseurs à la compréhension approfondie des différents statuts juridiques.<br /><br /> 
                            Au-delà de mon engagement dans le monde de l'entreprise, je nourris une passion inhabituelle pour la gendarmerie. Je crois fermement que les valeurs d'intégrité, de service et de responsabilité propres à la gendarmerie peuvent être intégrées dans l'écosystème entrepreneurial.
                        </p>
                    </div>
                </div>
            </div>
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
