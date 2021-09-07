<template>
  <div>
    <div class="container mx-auto px-4 lg:px-40">
      <div class="text-center">
        <p class="font-semibold text-lh-jungle-green leading-4 leading-8 mt-8 lg:mt-14 text-2xl lg:text-3xl">
          Listas de favoritos
        </p>
      </div>
      <div class="mt-14">
        <div class="flex flex-row lg:justify-start justify-evenly items-baseline flex-wrap">
          <HouseCard
            v-for="item in oneHausesList"
            :key="item.id"
            :img="item.attributes.real_estate_list[0].attributes.gallery_urls[0]"
            :imgAlt="item.attributes.name"
            :title="item.attributes.name"
            :description="item.attributes.real_estate_list.length + ' propiedad guardada'"
            url="/"
          />
          <HouseCard2
            v-for="item in twoHausesList"
            :key="item.id"
            :img1="item.attributes.real_estate_list[0].attributes.gallery_urls[0]"
            :img2="item.attributes.real_estate_list[1].attributes.gallery_urls[0]"
            :imgAlt="item.attributes.name"
            :title="item.attributes.name"
            :description="item.attributes.real_estate_list.length + ' propiedades guardadas'"
            url="/"
          />
          <HouseCard3
            v-for="item in threeHausesList"
            :key="item.id"
            :img1="item.attributes.real_estate_list[0].attributes.gallery_urls[0]"
            :img2="item.attributes.real_estate_list[1].attributes.gallery_urls[0]"
            :img3="item.attributes.real_estate_list[2].attributes.gallery_urls[0]"
            :imgAlt="item.attributes.name"
            :title="item.attributes.name"
            :counter="item.attributes.real_estate_list.length-2"
            :description="item.attributes.real_estate_list.length + ' propiedades guardadas'"
            url="/"
          />
          <div class="w-80 mb-14 px-4 py-2 hover:shadow-xl transition delay-150 duration-300 ease-in-out">
            <a class="block h-52 mb-5" href="/">
              <div class="bg-indigo-50 h-full rounded-lg relative">
                <img class="absolute inset-2/4 transform -translate-x-1/2 -translate-y-1/2"
                  src="~/assets/add-icon.svg" alt="Crear una nueva lista" />
              </div>
            </a>
            <h2 class="text-lg mb-1 font-semibold text-blue-600 text-center">
              Crear una nueva lista
            </h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HouseCard from "@/components/HouseCard/HouseCard.vue";
import HouseCard2 from "@/components/HouseCard/HouseCard2.vue";
import HouseCard3 from "@/components/HouseCard/HouseCard3.vue";
export default {
  data() {
    return {
      favoritesList: []
    };
  },
  layout: "favoritesList",
  async asyncData({ params, $http }) {
    const post = await $http.$get(
      "https://lh-real-estates-challenge-api.herokuapp.com/real-estates"
    );
    post.data.forEach(entity => {
      entity.attributes.real_estate_list = [];
      entity.attributes.real_estate_ids.forEach(id => {
        let index = post.included.findIndex(e => {
          return e.id == id;
        });
        if (index > -1) {
          entity.attributes.real_estate_list.push(post.included[index]);
        }
      });
    });

    return { favoritesList: post.data };
  },
  components: {
    HouseCard,
    HouseCard2,
    HouseCard3
  },
  computed: {
    oneHausesList: function() {
      return this.favoritesList.filter(function(entity) {
        return entity.attributes.real_estate_list.length < 2;
      });
    },
    twoHausesList: function() {
      return this.favoritesList.filter(function(entity) {
        return entity.attributes.real_estate_list.length === 2;
      });
    },
    threeHausesList: function() {
      return this.favoritesList.filter(function(entity) {
        return entity.attributes.real_estate_list.length > 2;
      });
    }
  }
};
</script>
