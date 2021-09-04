<!-- Please remove this file from your project -->
<template>
  <div class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0">
    <div class="max-w-4xl mx-auto sm:px-6 lg:px-8">
      <HausLogo size="hausLogo-2xl"/>
      <div class="mt-8 bg-white overflow-hidden shadow sm:rounded-lg p-6">
        <h1 class="text-2xl leading-7 font-semibold">
          ¡Bienvenido! Compra tu vivienda nueva
        </h1>
      </div>
    </div>
  </div>
</template>

<script>
import HausLogo from "@/components/HausLogo";
export default {
  components: {
    HausLogo
  }
};
</script>
