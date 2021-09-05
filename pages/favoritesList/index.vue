<template>
  <div>
    <div class="container mx-auto px-4 lg:px-40">
      <div class="text-center">
        <p class="font-semibold text-lh-jungle-green leading-4 leading-8 mt-8 lg:mt-14 text-3xl">
          Listas de favoritos
        </p>
      </div>
      <div class="mt-14">
        <div class="flex flex-row lg:justify-start justify-evenly items-baseline flex-wrap">
          <HomeCard v-for="item in favoritesList" :key="item.id"
            img="https://lh-sobreplanos-staging.imgix.net/uploads/real_estate_attachment/picture/4275620/uba_120_apartamentos_en_venta_en_santa_barbara_oriental_con_20m_gallery_0df5de59994bbcf41714.jpg"
            :imgAlt="item.attributes.name"
            :title="item.attributes.name"
            description="18 propiedades guardadas"
            url="/"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HomeCard from "@/components/HomeCard.vue";
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
    console.log(post);
    post.data.push( {
            "id": "43148555",
            "attributes": {
                "name": "Mis favoritos",
                "real_estate_ids": [
                    195748,
                    196996
                ]
            }
        })
    return { favoritesList: post.data };
  },
  components: {
    HomeCard
  }
};
</script>
