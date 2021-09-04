<template>
  <div>
    <nav
      class="flex items-baseline justify-between flex-wrap px-6 lg:px-16 py-5 border-b"
    >
      <div class="hidden lg:block mr-6">
          <HausLogo size="hausLogo-lg"/>
      </div>
      <div class="flex lg:hidden">
        <button
          class="flex relative items-center px-3 py-2 hover:text-white"
        >
          <img src="~/assets/bars.svg" title="ícono de barras"/> <div class="point point pointPosition-bars"></div
        >



        </button>
        <img src="~/assets/h-logo.svg" title="Logo" class="ml-1.5"/>
      </div>
      <div
        class="w-full hidden lg:block flex-grow lg:flex lg:w-auto items-end justify-end"
      >
        <a
          href="/"
          class="block mt-4 lg:inline-block lg:mt-0 hover:text-green-300 mr-4"
        >
          Cundinamarca</a
        >
        <a
          href="/"
          class="block mt-4 lg:inline-block lg:mt-0 hover:text-green-300 mr-4"
        >
          Antioquia</a
        >
        <a
          href="/"
          class="block mt-4 lg:inline-block lg:mt-0 hover:text-green-300"
        >
          Recursos</a
        >
        <a href="/" class="flex relative mt-4 lg:mt-0 font-medium lg:ml-4 mr-4">
          Mi Perfil <img src="~/assets/chevron-down.svg" title="ícono" class="ml-1.5"/>
          <div class="point pointPosition-chevron"></div
        ></a>
      </div>
    </nav>
  </div>
</template>

<style>
.point {
  background: #3ecfaf;
  height: 12px;
  width: 12px;
  border-radius: 50%;
}

.pointPosition-bars{
    position: absolute;
    left: 38px;
    top: 5px;
}

.pointPosition-chevron{
    position: absolute;
    left: 80px;
    top: -4px;
}
</style>

<script>
import HausLogo from "@/components/HausLogo";
export default {
  name: "TheHeader"
};
</script>
