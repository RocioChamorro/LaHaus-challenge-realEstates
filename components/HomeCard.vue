<template>
  <div class="w-80 mb-14 px-4 py-2 rounded-lg">
    <a class="block" :href="url"><img class="rounded-lg h-52 mb-5" :src="img" :alt="imgAlt" width="100%"></a>
    <h2 class="text-lg mb-1 font-semibold text-lh-jungle-green">{{ title }}</h2>
    <p class="text-lh-green-gray">{{ description }}</p>
  </div>
</template>

<script>
  export default {
    props: ['img', 'imgAlt', 'title', 'description', 'url']
  }
</script>