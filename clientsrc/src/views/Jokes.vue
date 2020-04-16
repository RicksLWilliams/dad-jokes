<template>
  <div class="jokes container-fluid">
    <h1>THIS IS THE JOKES PAGES</h1>
    <CreateJoke v-if="$auth.isAuthenticated" />
    <small class="text-danger" v-else>You must log in to create a joke.</small>
    <div class="row justify-content-around">
      <joke v-for="joke in jokes" :jokeData="joke" :key="joke._id"> do we see this</joke>
    </div>
  </div>
</template>


<script>
import CreateJoke from "../components/CreateJoke";
import Joke from "../components/Joke";
export default {
  name: "jokes",
  data() {
    return {};
  },
  mounted() {
    console.log(this.$auth);
    this.$store.dispatch("getJokes");
  },
  computed: {
    jokes(){
      return this.$store.state.jokes
    }
  },
  methods: {},
  components: { CreateJoke, Joke }
};
</script>


<style scoped>
</style>