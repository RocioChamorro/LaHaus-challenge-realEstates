<template>
  <div class="w-80 mb-14 px-4 py-2 rounded-lg">
    <a class="block h-52 mb-5 relative" :href="url">
      <div class="rounded-lg h-full bg-cover" :style="imageUrl"></div>
    </a>
    <h2 class="text-lg mb-1 font-semibold text-lh-jungle-green">{{ title }}</h2>
    <p class="text-lh-green-gray">{{ description }}</p>
  </div>
</template>

<script>
export default {
  computed: {
    imageUrl() {
      return { "background-image": "url('" + this.img + "')" };
    }
  },
  props: ["img", "imgAlt", "title", "description", "url"]
};
</script>