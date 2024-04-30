<template>
    <div class="bg-[url('/img/fond.png')] bg-fixed w-full min-h-screen h-fit bg-cover pt-10 relative">

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
                    <PhoneNavLink name="Accueil" link="/" @click="this.togglePhoneNav()" />
                    <PhoneNavLink name="Présentation" link="#about-me" @click="this.togglePhoneNav()" />
                    <PhoneNavLink name="Compétences" link="#skills" @click="this.togglePhoneNav()" />
                    <PhoneNavLink name="Mes projets" link="#my-projects" @click="this.togglePhoneNav()" />
                    <PhoneNavLink name="Contact" link="#contact" @click="this.togglePhoneNav()" />
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
    <div class="bg-gradient-to-b from-[#161B1F] to-[#010204] w-full h-fit relative" :class="this.isPhoneNavDisplay ? 'hidden' : 'block'">
        
        <RoundWhiteBlur class="absolute top-[400px]"/>
        <RoundWhiteBlur class="absolute top-[700px] right-0"/>
        <RoundWhiteBlur class="absolute top-[2100px]"/>

        <!-- About me -->
        <div class="pt-20 px-10 md:px-20 relative scroll-smooth" id="about-me">
            <h1 class="uppercase font-ZenTokyoZoo text-5xl sm:text-7xl md:text-8xl text-white leading-tight">A propos <br />de moi</h1>
            <img src="/img/shooting_star.png" alt="Etoile filante" class="hidden xl:block w-[500px] 2xl:w-auto absolute top-24 2xl:top-20 right-20" data-aos="slide-right">

            <div class="xl:mx-10 2xl:mx-40">
                <div class="xl:flex xl:gap-x-7 -translate-y-7 md:-top-10">
                    <img src="/img/photo_profil.png" alt="Etoile filante" class="mx-auto xl:mx-0 w-64 h-64 md:w-96 md:h-96 rounded-xl" data-aos="zoom-in">

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

                                <a href="https://www.linkedin.com/in/erwan-nicolas-79729029a/" target="_blank" class="hover:-translate-y-1 duration-300">
                                    <LinkedinIcon color="white" />
                                </a>
                                
                                <a href="https://github.com/NicoDev99" target="_blank" class="hover:-translate-y-1 duration-300">
                                    <GithubIcon color="white" />
                                </a>
                            </div>

                            <a href="/CV.pdf" download="CV.pdf" class="mx-auto mt-12 md:mt-0 md:mx-0 w-fit text-white cursor-pointer flex gap-x-2 border border-solid border-white px-3 py-2.5 rounded hover:bg-white/10 duration-500">
                                Télécharger CV
                                <PaperIcon color="white"/>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
            
            <!-- My course -->
            <div class="mt-32">
                <div>
                    <TitleSide>
                        <h1 class="font-ZenOldMincho text-white text-3xl">Mon parcours</h1>
                    </TitleSide>

                    <h2 class="font-Genos text-[#767478] max-w-xl mx-auto text-center mt-6 text-xs lg:text-lg">Passionné par le numérique depuis toujours, mon parcours témoigne de cette passion
                        pour la technologie, une histoire qui ne cesse de s'enrichir.</h2>
                </div>

                <div class="w-fit mx-auto relative">
                    <Satellite width="200" height="200" color="white" class="-rotate-90 hidden xl:block translate-x-20 translate-y-10"/>

                    <ExperienceElement number="1" orientation="left" class="translate-x-0 xl:translate-x-48 2xl:translate-x-64 mb-40 xl:mb-0 mt-24 xl:mt-0">
                        <div class="text-white w-full max-w-lg 2xl:max-w-xl" data-aos="fade-right">
                            <div class="flex justify-between items-center mb-3">
                                <h1 class="font-ZenDots text-sm lg:text-lg 2xl:text-xl">Fondateur - CEO</h1>
                                <p class="text-[#BDBDBD] text-xs 2xl:text-sm font-YujiSyuku text-right">juin 2023 - Aujourd’hui</p>
                            </div>
                            <p class="text-justify font-Roboto text-sm lg:text-base">Après avoir passé plusieurs années à travailler en tant qu'indépendant, j'ai pris la décision de lancer ma propre entreprise. 
                                Mon objectif est de donner vie à mes projets tout en collaborant avec d'autres entreprises, en leur proposant mes services pour 
                                la conception et le développement de solutions informatiques sur mesure.</p>
                        </div>
                    </ExperienceElement>

                    <ExperienceElement number="2" orientation="right" class="translate-x-0 xl:-translate-x-52 2xl:-translate-x-64 mt-10 mb-40 xl:mb-0">
                        <div class="text-white w-full max-w-lg 2xl:max-w-xl" data-aos="fade-left">
                            <div class="flex justify-between items-center mb-3">
                                <h1 class="font-ZenDots text-sm lg:text-lg 2xl:text-xl">Etudes entrepreneurials</h1>
                                <p class="text-[#BDBDBD] text-xs 2xl:text-sm font-YujiSyuku text-right">fev. 2024 - Aujourd’hui</p>
                            </div>
                            <p class="text-justify font-Roboto text-sm lg:text-base">Dans le cadre du programme PEPITE, j'ai rejoint la formation D2E pour approfondir mes compétences 
                                dans le domaine de l'entrepreneuriat et de la gestion de projet. Cette formation m'offre l'opportunité d'explorer en profondeur divers aspects 
                                tels que l'élaboration de plans d'affaires, les interactions avec les investisseurs, les aspects juridiques incluant les différents statuts 
                                possibles pour les entreprises, ainsi que les études de marché.</p>
                        </div>
                    </ExperienceElement>

                    <ExperienceElement number="3" orientation="left" class="translate-x-0 xl:translate-x-48 2xl:translate-x-64 mt-10 mb-40 xl:mb-0">
                        <div class="text-white w-full max-w-lg 2xl:max-w-xl" data-aos="fade-right">
                            <div class="flex justify-between items-center mb-3">
                                <h1 class="font-ZenDots text-sm lg:text-lg 2xl:text-xl">Développeur Web Full Stack</h1>
                                <p class="text-[#BDBDBD] text-xs 2xl:text-sm font-YujiSyuku text-right">oct. 2022 - Aujourd’hui</p>
                            </div>
                            <p class="text-justify font-Roboto text-sm lg:text-base">J'ai rejoint l'équipe d'INOCESS en alternance dans le but de contribuer à la création, la conception, le développement et 
                                la mise en œuvre d'une solution informatique permettant la visualisation de données sous diverses formes telles que des graphiques, des graphes et des matrices. </p>
                        </div>
                    </ExperienceElement>

                    <ExperienceElement number="4" orientation="right" class="translate-x-0 xl:-translate-x-52 2xl:-translate-x-64 mt-10 mb-40 xl:mb-0">
                        <div class="text-white w-full max-w-lg 2xl:max-w-xl" data-aos="fade-left">
                            <div class="flex justify-between items-center mb-3">
                                <h1 class="font-ZenDots text-sm lg:text-lg 2xl:text-xl">Etudes Supérieures</h1>
                                <p class="text-[#BDBDBD] text-xs 2xl:text-sm font-YujiSyuku text-right">sept. 2022 - Aujourd’hui</p>
                            </div>
                            <p class="text-justify font-Roboto text-sm lg:text-base">Après l'obtention de mon baccalauréat, j'ai rejoint le Bachelor Universitaire de Technologie (BUT) à l'IUT de Nice, 
                                sur le campus de Sophia Antipolis, dans le but d'approfondir mes compétences en informatique. Actuellement en deuxième année de BUT, cette 
                                formation m'a permis de faire des avancées significatives dans ce domaine aussi vaste que complexe</p>
                        </div>
                    </ExperienceElement>

                    <SatelliteDish width="175" height="175" color="white" class="-rotate-90 absolute right-24 hidden xl:block"/>
                </div>
            </div>
        </div>


        <!-- Skills -->
        <div class="mt-44 md:mt-96 pb-[600px] mx-10 relative" id="skills">

            <RoundWhiteBlur class="absolute top-[700px] right-0"/>

            <div class="w-fit mx-auto" >
                <Separator class="mx-auto mb-10" data-aos="zoom-in" data-aos-easing="linear"/>
                <h1 class="font-Syncopate text-white text-center text-2xl sm:text-4xl">Mes compétences</h1>
                <h2 class="font-Genos text-[#767478] max-w-xl mx-14 md:mx-auto text-center mt-6 text-xs lg:text-lg">Au file des années j'ai acquis une grande expérience dans différents langages qui ne cessent encore de me surprendre aujourd'hui par leurs nouveautés</h2>
            </div>

            <div class="md:columns-2 mx-0 lg:mx-20 2xl:mx-64 md:gap-x-14 lg:gap-x-28 mt-20">
                <LinearProgressBar firstColor="#F16529" endColor="#2965F1" progress="90" name="HTML/CSS"/>
                <ProgressBar color="#CF649B" progress="70" name="SASS/SCSS" class="mt-12" />
                <ProgressBar color="#4DB0B4" progress="90" name="TailWindCSS" class="mt-12" />
                <ProgressBar color="#FFD93D" progress="70" name="JavaScript" class="mt-12" />
                <ProgressBar color="#A259FF" progress="70" name="Figma" class="mt-12" />
                <ProgressBar color="#8993C1" progress="90" name="PHP" class="mt-12 lg:mt-0" />
                <ProgressBar color="#339ADB" progress="70" name="MySQL" class="mt-12" />
                <LinearProgressBar firstColor="#FE2C21" endColor="#63B586" progress="70" name="Laravel/VueJS" class="mt-12"/>
                <ProgressBar color="#FE767A" progress="50" name="ChartJS" class="mt-12" />
                <ProgressBar color="#A3EDBA" progress="50" name="Highcharts" class="mt-12" />
            </div>

            <div class="flex items-center mt-24">
                <Satellite width="125" height="125" color="rgba(255, 255, 255, 0.5)" class="-rotate-[135deg] hidden md:block"/>
                <p class="text-white/50 font-RobotoFlex text-sm lg:text-base text-center md:text-left">Mes compétences sont basées sur mon expérience professionnelle et sur les différents projets sur lesquels j’ai pu travailler</p>
            </div>
        </div>
    </div>
</template>


<script>
    import AOS from 'aos';
    import 'aos/dist/aos.css'

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
    import Satellite from './components/icons/Satellite.vue';
    import ExperienceElement from "./components/ExperienceElement.vue"
    import SatelliteDish from './components/icons/SatelliteDish.vue';
    import RoundWhiteBlur from './components/RoundWhiteBlur.vue';
    import ProgressBar from './components/ProgressBar.vue';
    import LinearProgressBar from './components/LinearProgressBar.vue';

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
            PaperIcon,
            Satellite,
            ExperienceElement,
            SatelliteDish,
            RoundWhiteBlur,
            ProgressBar,
            LinearProgressBar
        },

        setup() {
            AOS.init({
                once: true
            });
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