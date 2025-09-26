<template>
  <p class="font-bold text-center text-xl mt-10">
    Roupa que <span class="text-[#366C90]">respeita</span> sua luta
  </p>

  <div class="mt-5 p-2">
    <!-- Carrossel de Produtos -->
    <Swiper
      :modules="[Navigation, Pagination]"
      :slides-per-view="4"
      :space-between="1"
      :loop="true"
      :navigation="{ nextEl: '.button-next', prevEl: '.button-prev' }"
      pagination
      :breakpoints="{
        320: { slidesPerView: 1 },
        640: { slidesPerView: 2 },
        1024: { slidesPerView: 4 },
        1440: { slidesPerView: 5 },
      }"
      class="relative"
    >
      <SwiperSlide v-for="(product, index) in products" :key="index">
        <div class="bg-white w-72 rounded-xl p-4 mx-auto">
          <!-- Carrossel de imagens do produto -->
          <Swiper
            :modules="[Navigation]"
            :slides-per-view="1"
            :loop="true"
            :navigation="{ nextEl: '.custom-next', prevEl: '.custom-prev' }"
            class="rounded-lg mb-4 relative"
          >
            <SwiperSlide v-for="(image, i) in product.images" :key="i">
              <img
                :src="image"
                :alt="product.title"
                class="w-full h-72 object-cover rounded-lg"
              />
            </SwiperSlide>
            <button
              class="custom-prev absolute z-10 top-1/2 left-1 transform -translate-y-1/2 text-white p-1 rounded-full hover:bg-[#366C90] cursor-pointer"
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
                class="lucide lucide-chevron-left-icon lucide-chevron-left"
              >
                <path d="m15 18-6-6 6-6" />
              </svg>
            </button>
            <button
              class="custom-next absolute z-10 top-1/2 right-1 transform -translate-y-1/2 text-white p-1 rounded-full hover:bg-[#366C90] cursor-pointer"
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
                class="lucide lucide-chevron-right-icon lucide-chevron-right"
              >
                <path d="m9 18 6-6-6-6" />
              </svg>
            </button>
          </Swiper>

          <!-- Informações do produto -->
          <div class="text-start">
            <h2 class="text-lg font-bold">{{ product.title }}</h2>
            <p class="text-sm font-bold text-gray-500">
              {{ product.description }}
            </p>

            <div class="font-semibold flex items-center gap-2 mt-2">
              <p class="text-gray-400 line-through">R${{ product.antprice }}</p>
              <h1>R$ {{ product.price }}</h1>
            </div>
          </div>

          <button
            class="flex items-center justify-center gap-1 font-bold uppercase text-sm text-white w-full py-2 px-4 mt-2 bg-[#366C90] hover:scale-95 transition-all rounded-lg cursor-pointer"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 24 24"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
              class="size-5 lucide lucide-shopping-cart-icon lucide-shopping-cart"
            >
              <circle cx="8" cy="21" r="1" />
              <circle cx="19" cy="21" r="1" />
              <path
                d="M2.05 2.05h2l2.66 12.42a2 2 0 0 0 2 1.58h9.78a2 2 0 0 0 1.95-1.57l1.65-7.43H5.12"
              />
            </svg>
            Comprar
          </button>
        </div>
      </SwiperSlide>

      <button
        class="button-prev absolute z-10 top-1/2 left-1 transform -translate-y-1/2 text-[#366C90] bg-gray-100 shadow-md p-1 rounded-full hover:bg-gray-200 cursor-pointer"
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
          class="lucide lucide-chevron-left-icon lucide-chevron-left"
        >
          <path d="m15 18-6-6 6-6" />
        </svg>
      </button>
      <button
        class="button-next absolute z-10 top-1/2 right-1 transform -translate-y-1/2 text-[#366C90] bg-gray-100 shadow-md p-1 rounded-full hover:bg-gray-200 cursor-pointer"
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
          class="lucide lucide-chevron-right-icon lucide-chevron-right"
        >
          <path d="m9 18 6-6-6-6" />
        </svg>
      </button>
    </Swiper>
  </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation, Pagination } from "swiper/modules";

// Import Swiper CSS
import "swiper/css";
import "swiper/css/navigation";
import "swiper/css/pagination";

const products = [
  {
    title: "T-Shirt",
    description: "T-Shirt perfomace preta",
    antprice: "150,00",
    price: "99,99",
    images: [
      new URL("@/assets/products/tshirt-1.jpeg", import.meta.url).href,
      new URL("@/assets/products/tshirt-2.jpeg", import.meta.url).href,
    ],
  },
  {
    title: "Rash Guard",
    description: "Rash guard preta",
    antprice: "100,00",
    price: "79,99",
    images: [
      new URL("@/assets/products/rash-preta.jpeg", import.meta.url).href,
    ],
  },
  {
    title: "Rash Guard",
    description: "Rash guard branca",
    antprice: "100,00",
    price: "79,99",
    images: [
      new URL("@/assets/products/rash-branca.jpeg", import.meta.url).href,
    ],
  },
  {
    title: "Rash Guard",
    description: "Rash guard manga branca",
    antprice: "100,00",
    price: "79,99",
    images: [
      new URL("@/assets/products/rash-manga-branca.jpeg", import.meta.url).href,
    ],
  },
  {
    title: "Rash Guard",
    description: "Rash guard manga azul",
    antprice: "100,00",
    price: "79,99",
    images: [
      new URL("@/assets/products/rash-manga-azul.jpeg", import.meta.url).href,
    ],
  },
];
</script>

<style></style>
