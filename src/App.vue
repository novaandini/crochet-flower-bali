<template>
  <div class="bg-white">
    <header class="inset-x-0 top-0 z-50 fixed bg-white">
      <nav class="flex items-center justify-between px-6 py-2 lg:px-8" aria-label="Global">
        <div class="flex lg:flex-1">
          <a href="#" class="-m-1.5 p-1.5">
            <span class="sr-only">Your Company</span>
            <img class="h-14 w-auto" src="/src/assets/logo.jpg" alt="" />
          </a>
        </div>
        <div class="flex lg:hidden">
          <button type="button" class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = true">
            <span class="sr-only">Open main menu</span>
            <Bars3Icon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="hidden lg:flex lg:gap-x-12">
          <a v-for="item in navigation" :key="item.name" :href="item.href" class="text-sm/6 font-semibold text-gray-900">{{ item.name }}</a>
        </div>
      </nav>
      <Dialog class="lg:hidden" @close="mobileMenuOpen = false" :open="mobileMenuOpen">
        <div class="fixed inset-0 z-50" />
        <DialogPanel class="fixed inset-y-0 right-0 z-50 w-full overflow-y-auto bg-white px-6 py-6 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10">
          <div class="flex items-center justify-between">
            <a href="#" class="-m-1.5 p-1.5">
              <span class="sr-only">Your Company</span>
              <img class="h-14 w-auto" src="/src/assets/logo.jpg" alt="" />
            </a>
            <button type="button" class="-m-2.5 rounded-md p-2.5 text-gray-700" @click="mobileMenuOpen = false">
              <span class="sr-only">Close menu</span>
              <XMarkIcon class="h-6 w-6" aria-hidden="true" />
            </button>
          </div>
          <div class="mt-6 flow-root">
            <div class="-my-6 divide-y divide-gray-500/10">
              <div class="space-y-2 py-6">
                <a v-for="item in navigation" :key="item.name" :href="item.href" class="-mx-3 block rounded-lg px-3 py-2 text-base/7 font-semibold text-gray-900 hover:bg-gray-50">{{ item.name }}</a>
              </div>
            </div>
          </div>
        </DialogPanel>
      </Dialog>
    </header>

    <div class="relative isolate px-6 pt-14 lg:px-8 md:pt-20">
      <div class="absolute inset-x-0 -top-40 -z-10 transform-gpu overflow-hidden blur-3xl sm:-top-80" aria-hidden="true">
        <div class="relative left-[calc(50%-11rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 rotate-[30deg] bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%-30rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
      <img src="./assets/lily.jpg" alt="" srcset="" class="absolute -z-20 top-20 md:top-10 md:right-2/3 md:left-auto md:h-full left-0 brightness-50 md:filter-none">
      <img src="./assets/corgi.jpg" alt="" srcset="" class="absolute lg:-bottom-20 md:-bottom-14 lg:right-20 md:right-0 lg:w-1/5 md:w-1/4 hidden md:block">
      <div class="lg:py-40 py-28">
        <div class="flex justify-center items-center justify-self-end md:w-2/3">
          <div class="text-left">
            <h1 class="text-balance text-5xl font-semibold tracking-tight text-white md:text-gray-900 sm:text-7xl">Crochet Flower Bali</h1>
            <p class="mt-8 text-pretty text-justify text-lg font-medium text-gray-200 md:text-gray-500 sm:text-xl/8">Lengkapi keseharian Anda dengan produk lucu penuh warna dari katalog kami!</p>
            <div class="mt-5 flex items-center justify-left gap-x-6">
              <a href="#" class="rounded-md bg-indigo-600 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-indigo-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Lihat Katalog</a>
            </div>
          </div>
        </div>
      </div>
      <section id="about" class="bg-indigo-600 z-0 md:-z-10 relative isolate p-6 lg:p-8">
    <div class="flex flex-col justify-center items-center text-center min-h-screen">
      <div class="text-balance text-5xl font-semibold tracking-tight text-white sm:text-7xl order-first">
        About Us
      </div>
      <div class="bg-[url('/flower.jpg')] h-36 w-full mt-8 bg-[center_-12rem] md:bg-center md:row-span-3"></div>
      <div class="mt-8 text-pretty text-lg font-medium text-gray-200 sm:text-xl/8 order-last">Flower Crochet Bali menyediakan berbagai jenis bunga rajut yang lucu dan penuh warna. Temukan sentuhan spesial yang membuat hari-hari Anda lebih berwarna dengan Flower Crochet Bali!</div>
    </div>
  </section>

  <section id="products">
    <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
      <h2 class="text-balance text-5xl font-semibold text-center tracking-tight text-black sm:text-7xl">Products</h2>
      <div class="grid grid-cols-2 gap-x-6 gap-y-10 md:grid-cols-3 xl:grid-cols-4 xl:gap-x-8 mt-8">
        <a v-for="product in products" :key="product.id" :href="product.href" class="group">
          <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7">
            <img :src="product.imageSrc" :alt="product.imageAlt" class="h-full w-full object-cover object-center group-hover:opacity-75" />
          </div>
          <h3 class="mt-4 text-sm text-gray-700">{{ product.name }}</h3>
          <p class="mt-1 text-lg font-medium text-gray-900">{{ product.price }}</p>
        </a>
      </div>
    </div>
  </section>
      <div class="absolute inset-x-0 top-[calc(100%-13rem)] -z-10 transform-gpu overflow-hidden blur-3xl sm:top-[calc(100%-30rem)]" aria-hidden="true">
        <div class="relative left-[calc(50%+3rem)] aspect-[1155/678] w-[36.125rem] -translate-x-1/2 bg-gradient-to-tr from-[#ff80b5] to-[#9089fc] opacity-30 sm:left-[calc(50%+36rem)] sm:w-[72.1875rem]" style="clip-path: polygon(74.1% 44.1%, 100% 61.6%, 97.5% 26.9%, 85.5% 0.1%, 80.7% 2%, 72.5% 32.5%, 60.2% 62.4%, 52.4% 68.1%, 47.5% 58.3%, 45.2% 34.5%, 27.5% 76.7%, 0.1% 64.9%, 17.9% 100%, 27.6% 76.8%, 76.1% 97.7%, 74.1% 44.1%)" />
      </div>
    </div>
  </div>

</template>

<script setup>
const products = [
  {
    id: 1,
    name: 'Blue Theme Bouquet',
    href: '#',
    price: '$48',
    imageSrc: 'src/assets/products/blue-theme-bouquet.jpg',
    imageAlt: 'Blue theme bouquet',
  },
  {
    id: 2,
    name: 'Sunflower Bouquet',
    href: '#',
    price: '$35',
    imageSrc: 'src/assets/products/sunflower-bouquet.jpg',
    imageAlt: 'Sunflower Bouquet',
  },
  {
    id: 3,
    name: 'Josephine Basket',
    href: '#',
    price: '$89',
    imageSrc: 'src/assets/products/josephine-basket.jpg',
    imageAlt: 'Josephine Basket',
  },
  {
    id: 4,
    name: 'Small Bouquet',
    href: '#',
    price: '$35',
    imageSrc: 'src/assets/products/small-bouquet.jpg',
    imageAlt: 'Small bouquet',
  },
  // More products...
]

const links = [
  { name: 'Open roles', href: '#' },
  { name: 'Internship program', href: '#' },
  { name: 'Our values', href: '#' },
  { name: 'Meet our leadership', href: '#' },
]
const stats = [
  { name: 'Offices worldwide', value: '12' },
  { name: 'Full-time colleagues', value: '300+' },
  { name: 'Hours per week', value: '40' },
  { name: 'Paid time off', value: 'Unlimited' },
]

import { ref } from 'vue'
import { Dialog, DialogPanel } from '@headlessui/vue'
import { Bars3Icon, XMarkIcon } from '@heroicons/vue/24/outline'

const navigation = [
  { name: 'About', href: '#' },
  { name: 'Product', href: '#' },
  { name: 'Contact', href: '#' },
]

const mobileMenuOpen = ref(false)
</script>