<template>
  <header>
    <nav class="flex justify-between items-center py-3 px-5 font-bold">
      <ul class="sm:flex items-center gap-4 hidden">
        <li>
          <a
            href=""
            class="hover:text-sm hover:text-[#366C90] hover:underline underline-offset-4 decoration-2 decoration-[#366C90] transition-all"
            >T-Shirt</a
          >
        </li>
        <li>
          <a
            href=""
            class="hover:text-sm hover:text-[#366C90] hover:underline underline-offset-4 decoration-2 decoration-[#366C90] transition-all"
            >Rashs</a
          >
        </li>
        <li>
          <a
            href=""
            class="hover:text-sm hover:text-[#366C90] hover:underline underline-offset-4 decoration-2 decoration-[#366C90] transition-all"
            >Todos</a
          >
        </li>
      </ul>

      <div class="block sm:hidden">
        <button
          v-on:click="menuNav = !menuNav"
          class="text-[#366C90] p-2 cursor-pointer hover:scale-95 transition-all"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-menu-icon lucide-menu"
          >
            <path d="M4 5h16" />
            <path d="M4 12h16" />
            <path d="M4 19h16" />
          </svg>
        </button>

        <div v-show="menuNav" class="absolute bg-gray-100 w-72 rounded-lg">
          <ul class="p-2">
            <li>
              <a
                href=""
                class="p-1 hover:text-sm hover:text-[#366C90] hover:underline underline-offset-4 decoration-2 decoration-[#366C90] transition-all"
                >T-Shirt</a
              >
            </li>
            <li>
              <a
                href=""
                class="p-1 hover:text-sm hover:text-[#366C90] hover:underline underline-offset-4 decoration-2 decoration-[#366C90] transition-all"
                >Rashs</a
              >
            </li>
            <li>
              <a
                href=""
                class="p-1 hover:text-sm hover:text-[#366C90] hover:underline underline-offset-4 decoration-2 decoration-[#366C90] transition-all"
                >Todos</a
              >
            </li>
          </ul>
        </div>
      </div>

      <a href="">
        <img
          class="w-12 sm:w-16"
          src="../assets/logo-ikin.png"
          alt="logo itim"
        />
      </a>

      <div>
        <button
          class="text-[#366C90] p-2 cursor-pointer hover:scale-95 transition-all"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-search-icon lucide-search"
          >
            <path d="m21 21-4.34-4.34" />
            <circle cx="11" cy="11" r="8" />
          </svg>
        </button>

        <button
          class="text-[#366C90] p-2 cursor-pointer hover:scale-95 transition-all"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="lucide lucide-user-icon lucide-user"
          >
            <path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2" />
            <circle cx="12" cy="7" r="4" />
          </svg>
        </button>
      </div>
    </nav>

    <section class="font-bold grid sm:grid-cols-2 items-center py-3 px-5">
      <div class="text-start space-y-3">
        <p class="text-[#366C90] text-sm">Ikin Performace</p>
        <h1 class="text-3xl sm:text-6xl">
          Vista-se com a mesma
          <span class="text-[#366C90]">disciplina</span> que você leva para o
          <span class="text-[#366C90]">tatame</span>
        </h1>
        <p>
          Treine forte <span class="text-[#366C90] mx-2">Viva leve</span> Lute
          sempre
        </p>

        <div>
          <button
            class="text-white text-sm bg-[#366C90] p-2 rounded-full cursor-pointer hover:scale-95 transition-all"
          >
            Consultar
          </button>
        </div>
      </div>

      <div class="mt-4 sm:mt-0">
        <img src="../assets/modelos-ikin.png" alt="modelos" />
      </div>
    </section>

    <!-- <section
      class="flex justify-between items-center font-bold text-[#366C90] text-sm uppercase bg-gray-200 py-3 px-2 rounded-lg m-1"
    >
      <h1>Frete Gratis a partir de R$300</h1>
      <h1>Troca Rápida e Gratis</h1>
      <h1>10% OFF no Pix</h1>
    </section> -->
  </header>
</template>

<script>
export default {
  data() {
    return {
      menuNav: false,
    };
  },
};
</script>

<style></style>
