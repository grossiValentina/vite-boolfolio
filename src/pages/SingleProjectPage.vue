<script>
import axios from "axios";
import { store } from "../store";

export default {
  data() {
    return {

      store,
      project: null,
      loading: false
    };
  },
  created() {

    this.loading = true;

    axios.get(`${this.store.baseUrl}/api/projects/${this.$route.params.slug}`)
      .then((resp) => {
          this.project = resp.data.result;
      })

      .finally(() => {
       this.loading = false
    })
  },
};
</script>

<template>
  <div class="container mt-4">

    <div v-if="loading" >
        Caricamento del progetto...
    </div>

    <div v-else>
    
      <h3 class="text-center">{{ project.titolo }}</h3>
      <h6 class="m-3">Tecnologia: {{ project.technologies.nome }}</h6>
      <p>{{ project.descrizione }}</p>

    </div>
  </div>
</template>

<style lang="scss" scoped></style>