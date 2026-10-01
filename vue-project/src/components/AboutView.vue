<script setup>
defineEmits(['valt'])
</script>

<template>
  <div class="view">
    <h1>Alfa Bravo Charlie</h1>
    
    <!-- Ez a közös tároló a rugalmas elrendezéshez -->
    <div class="tartalom-blokk">
      
      <!-- A táblázat pontosan ugyanaz marad -->
      <div class="tablazat-container">
        <table>
          <thead>
            <tr>
              <th id="firstColumn">Betű</th>
              <th>Kódszó</th>
            </tr>
          </thead>
          <tbody>
            <tr><td>A</td><td>Alfa</td></tr>
            <tr><td>B</td><td>Bravo</td></tr>
            <tr><td>C</td><td>Charlie</td></tr>
            <tr><td>D</td><td>Delta</td></tr>
            <tr><td>E</td><td>Echo</td></tr>
            <tr><td>F</td><td>Foxtrot</td></tr>
            <tr><td>G</td><td>Golf</td></tr>
            <tr><td>H</td><td>Hotel</td></tr>
            <tr><td>I</td><td>India</td></tr>
            <tr><td>J</td><td>Juliett</td></tr>
            <tr><td>K</td><td>Kilo</td></tr>
            <tr><td>L</td><td>Lima</td></tr>
            <tr><td>M</td><td>Mike</td></tr>
            <tr><td>N</td><td>November</td></tr>
            <tr><td>O</td><td>Oscar</td></tr>
            <tr><td>P</td><td>Papa</td></tr>
            <tr><td>Q</td><td>Quebec</td></tr>
            <tr><td>R</td><td>Romeo</td></tr>
            <tr><td>S</td><td>Sierra</td></tr>
            <tr><td>T</td><td>Tango</td></tr>
            <tr><td>U</td><td>Uniform</td></tr>
            <tr><td>V</td><td>Victor</td></tr>
            <tr><td>W</td><td>Whiskey</td></tr>
            <tr><td>X</td><td>X-ray</td></tr>
            <tr><td>Y</td><td>Yankee</td></tr>
            <tr><td>Z</td><td>Zulu</td></tr>
          </tbody>
        </table>
      </div>

      <!-- Kép tárolója a táblázat mellett -->
      <div class="kep-container">
        <!-- Az assets mappába mentett kép beillesztése -->
        <img src="../assets/repulo.jpg" alt="Malév repülőgép" class="repulo-kep" />
        <p class="kep-alairas">A nemzetközi légiközlekedésben a NATO ábécé használata kötelező szabvány.</p>
      </div>

    </div>

    <!-- Alsó navigációs link -->
    <footer class="oldal-alj">
      <a href="#" @click.prevent="$emit('valt', 'home')">Vissza a szöveghez</a>
    </footer>
  </div>
</template>

<style scoped>
/* A rugalmas elrendezés: egymás mellé teszi a táblázatot és a képet */
.tartalom-blokk {
  display: flex;
  gap: 30px; /* Távolság a táblázat és a kép között */
  align-items: flex-start; /* Fentről igazítja őket egy vonalba */
}

.tablazat-container {
  flex: 1; /* A táblázat kitölti a rendelkezésre álló hely nagy részét */
}

.kep-container {
  width: 350px; /* Fix szélesség a képnek és a szövegének, megegyezik a css-ed első oszlop méretével */
}

.repulo-kep {
  width: 100%; /* Kitölti a kep-container szélességét */
  height: auto;
  border-radius: 4px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  border: 1px solid black;
}

.kep-alairas {
  font-size: 14px;
  font-style: italic;
  text-align: center;
  margin-top: 8px;
  color: #1e3a8a;
}

/* A te eredeti táblázat formázási szabályaid */
#firstColumn {
  width: 100px;
}

table {
  width: 100%;
  border: 1px solid black;
  border-collapse: collapse;
  text-align: left;
  background-color: rgba(255, 255, 255, 0.4);
}

th, td {
  padding: 6px 10px;
  border: 1px solid black;
}

th {
  background-color: rgba(0, 0, 139, 0.1);
}

.oldal-alj {
  margin-top: 40px;
  padding-top: 15px;
  text-align: center;
  width: 100%;
}

/* Reszponzivitás: Ha keskeny a képernyő, a kép a táblázat alá ugrik */
@media (max-width: 768px) {
  .tartalom-blokk {
    flex-direction: column;
    align-items: center;
  }
  .kep-container {
    width: 100%;
    max-width: 400px;
  }
}
</style>