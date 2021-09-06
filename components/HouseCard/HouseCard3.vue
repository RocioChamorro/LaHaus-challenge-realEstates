<template>
  <div class="w-80 mb-14 px-4 py-2 rounded-lg">
    <a class="block h-52 mb-5 relative" :href="url">
      <div class="rounded-lg absolute h-full z-20 w-3/6 bg-cover border border-white" :style="imageUrl_1"></div>
      <div class="rounded-lg absolute h-full z-10 left-28 w-2/5 bg-cover border border-white" :style="imageUrl_2"></div>
      <div class="rounded-lg absolute h-full z-0 right-0 w-2/5 bg-cover bg-lh-jungle-green bg-blend-soft-light" :style="imageUrl_3">
        <div class="absolute w-10 text-base font-semibold text-center text-white bottom-1/2 right-2.5 transform translate-y-2/4">+ {{ counter }}</div>
      </div>
    </a>
    <h2 class="text-lg mb-1 font-semibold text-lh-jungle-green">{{ title }}</h2>
    <p class="text-lh-green-gray">{{ description }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    imageUrl_1() {
      return { "background-image": "url('" + this.img1 + "')" };
    },
    imageUrl_2() {
      return { "background-image": "url('" + this.img2 + "')" };
    },
    imageUrl_3() {
      return { "background-image": "url('" + this.img3 + "')" };
    }
  },
  props: ["img1", "img2", "img3", "imgAlt", "title", "counter", "description", "url"]
};
</script>
