<script setup>
// Definiáljuk az eseményt, amit a szülő App.vue felé küldünk
defineEmits(['valt'])
</script>

<template>
  <div class="view">
    <h1>Alfa Bravo Charlie</h1>
    <p>
      A NATO fonetikus <a href="#" @click.prevent="$emit('valt', 'about')">ábécé</a>, vagy hivatalos nevén az IRSA (International Radiotelephony Spelling Alphabet) 
      a jelenleg legszélesebb körben használt és legelterjedtebb betűzési rendszer az angol nyelvterületen. 
      Elsődlegesen azzal a céllal fejlesztették ki és tették mindenekelőtt katonai távközlési szabvánnyá, 
      hogy az élőszóban váltott üzenetekben szereplő betűk és számjegyek egyértelműen, félreértést kizáróan hangozzanak el. 
      Ha szeretnéd látni a teljes listát és a betűk kódjait, tekintsd meg a részletes fonetikus 
      <!-- Hagyományos link, ami oldalújratöltés nélkül vált komponenst -->
      <a href="#" @click.prevent="$emit('valt', 'about')">ábécé</a> táblázatot.
    </p>
    <p>
      Bár eredetileg katonai célra szánták, elterjedt és általánosan használttá vált minden olyan területen, 
      ahol az angol a kommunikáció nyelve. Talán a legnagyobb és legösszetettebb ilyen terület a nemzetközi 
      légiközlekedés és légiforgalom irányítás.
    </p>
  </div>
</template>