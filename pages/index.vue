<template>
  <Welcome />
</template>

<script>
export default {
  methods: {
    goToFavoritesList() {
      const router = this.$router;
      setTimeout(function() {
        router.push("/favoritesList");
      }, 1000);
    }
  },
  created() {
    this.goToFavoritesList();
  }
};
</script>
