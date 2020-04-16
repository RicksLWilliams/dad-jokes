<template>
  <div class="joke border m-3 mb-5 col-5 align-self-end">
      <p>{{jokeData.setup}}</p>

    <div class="dropdown m-2">
  <button class="btn btn-info dropdown-toggle" type="button" id="dropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    show punchline
  </button>
  <div class="dropdown-menu" aria-labelledby="dropdownMenuButton">
    <a class="dropdown-item" href="#">{{jokeData.punchline}}</a>

  </div>
</div>
  </div>
</template>

<script>
export default {
  name: "joke",
  props: ["jokeData"],
  data() {
    return {};
  },
  methods: {
  }
};
</script>

<style>
.joke {
  outline: 1px solid black;
}

.hovershow{
  display: none;
}

</style>