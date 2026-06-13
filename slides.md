---
theme: default
title: Maßnahmen zur Gewährleistung der Informationssicherheit bei der Anwendungsprogrammierung
class: text-center
drawings:
  persist: false
transition: fade
comark: true
aspectRatio: 16/9
---

# Maßnahmen zur Gewährleistung der Informationssicherheit bei der Anwendungsprogrammierung

Informationssicherheit I

---

# Agenda

- Motivation
- Secrets und Umgebungsvariablen
- Client- versus Serverlogik
- Datenvalidierung
- Zugänglichkeit von Daten
- Authentifizierung und Autorisierung

---

# Motivation

Datenleck bei VW

<div class="relative">
  <div class="flex flex-row justify-between">
    <div class="flex flex-col">
      <ul>
        <li>
          Daten zu 800.000 Elektrofahrzeugen
          <Arrow v-click x1="320" y1="15" x2="500" y2="50" />
        </li>
        <li>
          präzise Standortdaten zu 460.000 Fahrzeugen
          <Arrow v-after x1="400" y1="48" x2="500" y2="50" />
        </li>
        <li>
          Kontaktinformationen zu den Besitzern
          <Arrow v-after x1="335" y1="80" x2="500" y2="50" />
        </li>
      </ul>
    </div>
    <div class="flex flex-col flex-grow justify-center">
      <div v-after class="text-2xl text-center">
        öffentlich zugänglich
      </div>
    </div>
  </div>
  <span v-click class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 rotate-[-20deg] text-white bg-red-500 text-4xl font-bold text-center rounded-md">
    Verstoß gegen Schutzziel der Vertraulichkeit
  </span>
</div>

<div class="w-full">
  <img src="./public/images/VW.jpg" alt="VW-Logo" class="size-70 m-auto" title="Quelle: https://www.volkswagen-newsroom.com/de/bilder/detail/volkswagen-logo-30145">
</div>
