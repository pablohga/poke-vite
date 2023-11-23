<template>
  <div class="col-4">
    <div class="card p-2 mb-3 cardListPokemon">
      <p class="text-center">{{ pokemon.name }}</p>
      <img
              :src="urlBaseSvg"
              class="card-img-top"
              alt="..."
              height="80"
            />
    </div>
  </div>
</template>

<script setup>
const pokemon = defineProps(["name", "urlBaseSvg"])

</script>

<style scoped>
.cardListPokemon{
  background: rgb(145,63,251);
  background: radial-gradient(circle, rgba(145,63,251,0.9164915966386554) 0%, rgba(70,239,252,0.3) 100%);
  cursor: pointer;
}
.cardListPokemon:hover{
  background: rgb(145,63,251);
  background: radial-gradient(circle, rgba(145,63,251,2) 0%, rgba(70,239,252,0.8) 100%);
  cursor: pointer;
}
.cardListPokemon img:hover{ 
  padding: .2rem;
}

</style>