<template>
  <nav
    class="sticky top-0 z-50 flex flex-wrap items-center justify-between px-2 py-1 bg-kldarkblue mb-3 border-b-2 border-klblue">
    <div class="container px-4 mx-auto flex flex-wrap items-center justify-between">
      <div class="w-full relative flex justify-between lg:w-auto  px-4 lg:static lg:block lg:justify-start">
        <a class="text-3xl font-semibold leading-relaxed inline-block mr-4 py-2 whitespace-nowrap text-klwhite" href="#">
          Katsu
        </a>
        <button
          class="text-klwhite cursor-pointer text-xl leading-none px-3 py-1 border border-solid border-transparent rounded bg-transparent block lg:hidden outline-none focus:outline-none"
          type="button" v-on:click="toggleNavbar()">
          <i class="fas fa-bars"></i>
        </button>
      </div>
      <div v-bind:class="{ 'hidden': !showMenu, 'flex': showMenu }" class="lg:flex lg:flex-grow items-center">
        <ul class="flex flex-col lg:flex-row list-none ml-auto">
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-md leading-snug text-klwhite hover:text-kldarkblue" href="#">
              <span class="ml-2 font-semibold">Sobre</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-md leading-snug text-klwhite hover:text-kldarkblue"
              href="#Habilidades">
              <span class="ml-2 font-semibold">Habilidades</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-md leading-snug text-klwhite hover:text-kldarkblue"
              href="#Experiencia">
              <span class="ml-2 font-semibold">Experiência</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-md leading-snug text-klwhite hover:text-kldarkblue"
              href="#Projetos">
              <span class="ml-2 font-semibold">Projetos</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="px-3 py-2 flex items-center text-md leading-snug text-klwhite hover:text-kldarkblue "
              href="#Contato">
              <span class="ml-2 font-semibold">Contato</span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "neutral-navbar",
  data() {
    return {
      showMenu: false
    }
  },
  methods: {
    toggleNavbar: function () {
      this.showMenu = !this.showMenu;
    }
  }
}
</script>