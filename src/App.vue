<template>
  <div id="app">
    <h2>Array of strings</h2>
    <div class="options">
      <p><b>Options:</b></p>
      <div>
        <input type="checkbox" v-model="searchableName">
        searchable
      </div>
    </div>
    <VSelect v-model="selectedName" :options="names" :searchable="searchableName" />
    <h2>Array of objects</h2>
    <div class="options">
      <p><b>Options:</b></p>
      <div>
        <input type="checkbox" v-model="searchableContinent">
        searchable
      </div>
    </div>
    <VSelect v-model="selectedContinent" :options="contients" :searchable="searchableContinent" />
  </div>
</template>

<script>
import VSelect from "@/vue-bootstrap-select";

export default {
  name: "App",
  components: {
    VSelect
  },
  data() {
    return {
      names: [
        "John Doe",
        "Olive Yew",
        "Aida Bugg",
        "Teri Dactyl",
        "Paige Turner"
      ],
      contients: [
        { value: 0, text: "Africa" },
        { value: 1, text: "America" },
        { value: 2, text: "Asia" },
        { value: 3, text: "Europe" },
        { value: 4, text: "Oceania" }
      ],
      selectedName: null,
      searchableName: false,
      selectedContinent: null,
      searchableContinent: false
    };
  }
};
</script>


<style lang="scss" scoped>
#app {
  font-family: "Roboto", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 2em 1em;
}

.options {
  text-align: left;
  padding: 1em 0em;
}
</style>
