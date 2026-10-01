<script setup>
import { ref } from 'vue'
import HomeView from './components/HomeView.vue'
import AboutView from './components/AboutView.vue'

// 'home' = Főoldal (szöveg), 'about' = Részletek (táblázat)
const aktualisLap = ref('home')

// Egy egyszerű függvény, amivel a komponensek jelezni tudják a lapváltást
const navigacio = (lapNev) => {
  aktualisLap.value = lapNev
}
</script>

<template>
  <div id="app-container">
    <main>
      <!-- Megjelenítjük a megfelelő komponenst és átadjuk neki a váltás képességét -->
      <HomeView v-if="aktualisLap === 'home'" @valt="navigacio" />
      <AboutView v-else @valt="navigacio" />
    </main>
  </div>
</template>

<style>
/* A megadott CSS stílusok globális alkalmazása */
body {
  background-color: LightSkyBlue;
  color: darkblue;
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 20px;
}

#app-container {
  max-width: 800px;
  margin: 40px auto;
}

h1 {
  text-align: center;
}

p {
  text-align: justify;
  line-height: 1.6;
}

a {
  color: firebrick;
  text-decoration: underline;
  cursor: pointer;
}

a:hover {
  color: darkred;
}
</style>

















<!-- <script setup>
import { ref } from 'vue'

// 'home' = Kezdőlap, 'abc' = a betűzés
const aktualisLap = ref('home')
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
    </div>
  </header>

  <main>
    <TheWelcome />
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
 -->