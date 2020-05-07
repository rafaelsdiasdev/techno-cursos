<template>
  <div>
    <div v-if="loading">
      <PageLoading />
    </div>
    <transition>
      <div v-if="api">
        <h1>{{api.titulo}}</h1>
      </div>
    </transition>
  </div>
</template>

<script>
import fetchData from "@/mixins/fetchData";
export default {
  name: "cusos",
  mixins: [fetchData],

  created() {
    this.fetchData("/cursos");
  }
};
</script>

<style>
</style>