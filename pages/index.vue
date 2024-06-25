<template>
  <div>
    <div class="bg-[url('/img/fond.png')] bg-fixed w-full min-h-screen h-fit bg-cover pt-10 relative">

      <!-- Computer screen nav menu -->
      <nav class="border-y borer-solid border-[#767478] mx-auto w-5/6 py-3 max-w-5xl hidden lg:flex items-center justify-center">
        <IconsLogo width="30" height="30" class="mr-12"/>
        <ul class="flex gap-x-10">
          <NavLinkComuter name="Accueil" link="/" number="01" />
          <NavLinkComuter name="Présentation" link="#about-me" number="02" />
          <NavLinkComuter name="Compétences" link="#skills" number="03" />
          <NavLinkComuter name="Mes projets" link="#projects" number="04" />
          <NavLinkComuter name="Contact" link="#contact" number="05" />
        </ul>
      </nav>

      <!-- Phone screen nav menu -->
      <div class="block lg:hidden overflow-hidden">
        <div class="flex justify-between items-center mx-12">
          <IconsBurger width="40" height="40" color="white" class="cursor-pointer" @click="this.togglePhoneNav()"/>
          <IconsLogo width="40" height="40"/>
        </div>
        <nav class="bg-[#151A1E] w-full absolute top-0 transition ease duration-300 z-10" :class="!this.isPhoneNavDisplay ? '-translate-y-full' : '-translate-y-0 min-h-screen h-fit'">
          <IconsClose width="40" height="40" color="white" class="cursor-pointer mt-12 ml-10" @click="this.togglePhoneNav()" />
          <ul class="text-center mt-20">
            <IconsLogo height="60" width="60" class="block w-16 mx-auto mb-16"/>
            <NavLinkPhone name="Accueil" link="/" @click="this.togglePhoneNav()" />
            <NavLinkPhone name="Présentation" link="#about-me" @click="this.togglePhoneNav()" />
            <NavLinkPhone name="Compétences" link="#skills" @click="this.togglePhoneNav()" />
            <NavLinkPhone name="Mes projets" link="#projects" @click="this.togglePhoneNav()" />
            <NavLinkPhone name="Contact" link="#contact" @click="this.togglePhoneNav()" />
          </ul>
        </nav>
      </div>

      <div class="block text-center pb-44">
        <IconsArrow color="white" class="block m-auto mt-24 animate-bounce" />

        <TitlesSides class="mt-16">
          <h1 class="font-Habibi text-white text-2xl sm:text-4xl uppercase translate-y-6 animate-[transformBottomTop_1s_ease_forwards]">Erwan Nicolas</h1>
        </TitlesSides>

        <h2 class="text-white font-Gruppo mt-6 text-xl sm:text-3xl translate-y-6 animate-[transformBottomTop_1s_ease_forwards]">Développeur Web Full-Stack</h2>

        <Separator class="block mx-auto mt-12 translate-y-6 animate-[transformBottomTop_1s_ease_forwards]"/>
      </div>

      <a href="#about-me" class="block mx-auto absolute bottom-10 left-0 right-0 cursor-pointer border border-solid border-white rounded-full w-fit">
        <IconsArrow color="white" class="animate-[transformTopBottom_1s_ease] my-1.5 px-1 sm:px-0 sm:mx-1 sm:my-2.5" />
      </a>
    </div>
  </div>
</template>