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

        <a href="#about-me" class="block mx-auto absolute bottom-10 left-0 right-0 cursor-pointer border border-solid border-white rounded-full w-fit">
            <ArrowIcon color="white" class="animate-[transformTopBottom_1s_ease] my-1.5 px-1 sm:px-0 sm:mx-1 sm:my-2.5" />
        </a>
    </div>


    <!-- Bg linear gradient -->
    <div class="bg-gradient-to-b from-[#161B1F] to-[#010204] w-full h-auto" :class="this.isPhoneNavDisplay ? 'hidden' : 'block'">
        
        <!-- About me -->
        <div class="pt-20 px-10 md:px-20 pb-[600px] relative scroll-smooth" id="about-me">
            <h1 class="uppercase font-ZenTokyoZoo text-5xl sm:text-7xl md:text-8xl text-white leading-tight">A propos <br />de moi</h1>
            <img src="/img/shooting_star.png" alt="Etoile filante" class="hidden xl:block w-[500px] 2xl:w-auto absolute top-24 2xl:top-20 right-20 animate-[shootingStar_1s_ease]">

            <div class="relative pb-96 xl:mx-10 2xl:mx-40">
                <div class="xl:flex xl:gap-x-7 absolute -top-5 md:-top-10">
                    <img src="/img/photo_profil.png" alt="Etoile filante" class="mx-auto xl:mx-0 w-64 h-64 md:w-96 md:h-96 rounded-xl animate-[transformBottomTop_1s_ease]">

                    <div class="mx-0 sm:mx-10 lg:mx-40 xl:mx-0 mt-12 xl:mt-0">
                        <h1 class="font-ZenOldMincho text-4xl 2xl:text-5xl text-white text-center xl:text-left">Erwan Nicolas</h1>
                        <h2 class="text-white font-Gruppo mt-3 text-xl 2xl:text-2xl text-center xl:text-left">Développeur Web Full-Stack</h2>

                        <p class="font-Roboto text-white text-justify text-xs md:text-sm mt-7">
                            Etudiant en alternance en BUT Informatique à l'Université Côte d'Azur, je me distingue par ma passion polyvalente pour le développement, les nouvelles technologies, l'entrepreneuriat et la gendarmerie.<br /><br />
                            Je suis actuellement membre du prestigieux programme PEPITE, où je renforce mes compétences en entrepreneuriat au sein de la formation D2E. Mon expertise s'étend du développement informatique à l'élaboration de plans d'affaires, en passant par l'interaction avec les investisseurs et la compréhension approfondie des statuts juridiques. Parallèlement à mon engagement entrepreneurial, je nourris une passion singulière pour la gendarmerie. Je crois fermement que les valeurs d'intégrité, de service et de responsabilité propres à la gendarmerie peuvent enrichir l'écosystème entrepreneurial.
                        </p>

                        <div class="md:flex md:justify-between md:items-center mt-8">
                            <div class="flex gap-x-6 justify-center md:justify-normal">
                                <a href="/" target="_blank" class="hover:-translate-y-1 duration-300">
                                    <InstagramIcon color="white" />
                                </a>

                                <a href="/" target="_blank" class="hover:-translate-y-1 duration-300">
                                    <LinkedinIcon color="white" />
                                </a>
                                
                                <a href="/" target="_blank" class="hover:-translate-y-1 duration-300">
                                    <GithubIcon color="white" />
                                </a>
                            </div>

                            <a href="/" class="mx-auto mt-12 md:mt-0 md:mx-0 w-fit text-white cursor-pointer flex gap-x-2 border border-solid border-white px-3 py-2.5 rounded hover:px-4 hover:bg-white/10 duration-500">
                                Télécharger CV
                                <PaperIcon color="white"/>
                            </a>
                        </div>
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
    import InstagramIcon from './components/icons/Instagram.vue';
    import LinkedinIcon from "./components/icons/Linkedin.vue"
    import GithubIcon from "./components/icons/Github.vue"
    import PaperIcon from "./components/icons/Paper.vue"

    export default {
        components: {
            CompNavLink,
            BurgerIcon,
            PhoneNavLink,
            CloseIcon,
            Logo,
            ArrowIcon,
            Separator,
            TitleSide,
            InstagramIcon,
            LinkedinIcon,
            GithubIcon,
            PaperIcon
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
            },

        }
    }
</script>

<style>
/* .test:hover {
    box-shadow: inset 10.5em 0 0 0 white;
    transition: ease 1s;
} */

/* .btn {
  position: relative;
  display: inline-block;
  border: 2px solid transparent;
  transition: 250ms ease-out;
  cursor: pointer;
}

.btn span, .btn::after {
  color: white;
  position: relative;
  z-index: 1;
}

.btn::before {
  content: "";
  position: absolute;
  display: block;
  width: calc(100% + 2px);
  height: calc(100% + 2px);
  top: -1px;
  left: -1px;
  background: #f5f5ff;
}

.buttonX {
  border-color: white;
}
.buttonX span {
  color: white;
}
.buttonX::before {
  background: white;
  transform: scaleX(0);
  transform-origin: right;
  transition: transform 0.2s ease-out;
}
.buttonX:hover {
  border-color: white;
}
.buttonX:hover span {
  color: black;
}
.buttonX:hover::before {
  transform: scaleX(1);
  transform-origin: left;
} */
</style>