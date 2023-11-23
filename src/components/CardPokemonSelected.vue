<script setup>
 const pokemon = defineProps(['name','xp','height', 'img', 'loading'])
</script>

<template>
  <div 
    class="card CardPokemonSelected"
    :class="loading ? '' : 'animate__animated animate__flipInY'"
  >
            <img
              :src="pokemon.img"
              class="card-img-top pt-2"
              height="250"
              :alt="pokemon.name"
            />
            <div class="card-body">
              <h5 class="card-title text-center">{{ pokemon.name }}</h5>
              <hr>
              <div class="row">
                <section class="col">
                  <strong>XP: </strong>
                  <span>{{ pokemon.xp }}</span>
                </section>
                <section class="col">
                  <strong>Altura: </strong>
                  <span>{{ pokemon.height }}</span>
                </section>
              </div>
            </div>
          </div> 
</template>
 

 
<style scoped>
 .CardPokemonSelected{
  height: 450px;
  background: rgb(145,63,251);
  background: radial-gradient(circle, rgba(0, 60, 255, 0.916)0%, rgba(0, 149, 255, 0.3) 100%);
 }
</style>