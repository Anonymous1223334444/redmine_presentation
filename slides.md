---
theme: seriph
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
class: 'text-center'
highlighter: shiki
lineNumbers: false
info: |
  ## Redmine : Gérer Projets & Bugs
  Présentation pour le cours de Qualité Logicielle
drawings:
  persist: false
css: unocss
title: Redmine - Gestion de Projet et Suivi des Anomalies
transition: slide-left
---

# Redmine : Gérer Projets & Bugs Facilement

<div
  v-motion
  :initial="{ opacity: 0, y: 100 }"
  :enter="{ opacity: 1, y: 0, transition: { delay: 300, duration: 1000 } }"
  class="text-orange-400 text-5xl font-bold mt-4 mb-8"
>
  L'outil qui met de l'ordre dans vos projets logiciels
</div>

<div
  v-motion
  :initial="{ opacity: 0 }"
  :enter="{ opacity: 1, transition: { delay: 800 } }"
  class="pt-10 text-lg"
>
  <div class="bg-orange-500 text-white px-4 py-2 rounded-lg inline-block">
    Qualité Logicielle - André Sarr - Rachelle Ndour
  </div>
</div>

<div class="abs-br m-6 flex gap-2">
  <a href="https://www.redmine.org" target="_blank" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-launch />
  </a>
</div>

<style>
.slidev-layout {
  background-color: rgba(0, 0, 0, 0.4);
  background-blend-mode: darken;
}

h1, h2, h3 {
  background-image: linear-gradient(45deg, #ff6b6b 10%, #feca57 50%, #ff9f43 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 400% 400%;
  animation: gradient 15s ease infinite;
}

@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.slidev-layout.default {
  h1 + p {
    @apply opacity-100;
  }
}

.grid-item {
  @apply transition-all duration-300 hover:scale-105 hover:shadow-xl;
}

img {
  @apply rounded-lg shadow-lg;
}

ul li {
  @apply transition-all duration-200 hover:translate-x-2;
}

.icon-btn {
  @apply transition-all duration-200 hover:text-orange-400;
}
</style>

---
layout: center
class: text-center
---

# <span class="text-3xl font-bold text-[#2B90B6]">Au programme</span>

<div class="grid grid-cols-3 gap-8 mt-12 max-w-5xl mx-auto">
  <div class="bg-purple-900 bg-opacity-60 p-6 rounded-xl shadow-lg transform transition-transform hover:scale-105">
    <div class="text-4xl font-bold mb-2">01</div>
    <div class="text-2xl font-bold mb-2">Le Constat</div>
    <div class="text-base opacity-90">Pourquoi on a besoin d'outils ?</div>
  </div>

  <div class="bg-purple-900 bg-opacity-60 p-6 rounded-xl shadow-lg transform transition-transform hover:scale-105">
    <div class="text-4xl font-bold mb-2">02</div>
    <div class="text-2xl font-bold mb-2">L'Idée Redmine</div>
    <div class="text-base opacity-90">À quoi ça sert ?</div>
  </div>

  <div class="bg-purple-900 bg-opacity-60 p-6 rounded-xl shadow-lg transform transition-transform hover:scale-105">
    <div class="text-4xl font-bold mb-2">03</div>
    <div class="text-2xl font-bold mb-2">Gérer le Projet</div>
    <div class="text-base opacity-90">Comment organiser le travail ?</div>
  </div>

  <div class="bg-purple-900 bg-opacity-60 p-6 rounded-xl shadow-lg transform transition-transform hover:scale-105">
    <div class="text-4xl font-bold mb-2">04</div>
    <div class="text-2xl font-bold mb-2">Suivre les Bugs</div>
    <div class="text-base opacity-90">Comment ne rien laisser passer ?</div>
  </div>

  <div class="bg-purple-900 bg-opacity-60 p-6 rounded-xl shadow-lg transform transition-transform hover:scale-105">
    <div class="text-4xl font-bold mb-2">05</div>
    <div class="text-2xl font-bold mb-2">Redmine & Qualité</div>
    <div class="text-base opacity-90">Pourquoi c'est bon pour le logiciel ?</div>
  </div>

  <div class="bg-purple-900 bg-opacity-60 p-6 rounded-xl shadow-lg transform transition-transform hover:scale-105">
    <div class="text-4xl font-bold mb-2">06</div>
    <div class="text-2xl font-bold mb-2">Démonstration</div>
    <div class="text-base opacity-90">Voyons ça en vrai !</div>
  </div>
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">01. Le Constat : Faire un Logiciel, C'est Complexe !</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-software-resource />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Le Défi du Développement</span>

<div class="mr-10">

## <carbon-group class="inline-block mr-2" /> Organiser le Travail d'Équipe

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-user-multiple class="inline-block mr-2 text-orange-400" /> Plusieurs personnes travaillent ensemble.</li>
  <li><carbon-task class="inline-block mr-2 text-orange-400" /> Il y a plein de tâches différentes à faire.</li>
  <li><carbon-help class="inline-block mr-2 text-orange-400" /> Qui fait quoi ? Quand ?</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <img src="https://media.istockphoto.com/id/1266413326/fr/vectoriel/signe-de-d%C3%A9fi-vectoriel-pop-art-bulle-de-la-parole-comique-avec-la-concurrence-de-texte.jpg?s=612x612&w=0&k=20&c=TL0dxPC4A08GDhDI1Syduzg2YPvFA6AiNSfhAA42XiI=" class="rounded-xl shadow-2xl max-h-[60vh] object-cover" />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Le Défi du Développement</span>

<div class="mr-10">

## <carbon-debug class="inline-block mr-2" /> Gérer les Problèmes (les "Bugs")

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-warning-alt class="inline-block mr-2 text-orange-400" /> Les erreurs arrivent, c'est normal !</li>
  <li><carbon-search class="inline-block mr-2 text-orange-400" /> Il faut les trouver, les comprendre et les corriger.</li>
  <li><carbon-checkbox-checked class="inline-block mr-2 text-orange-400" /> Comment être sûr de n'en oublier aucun ?</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <img src="https://media.giphy.com/media/xTiTnGeUsWOEwsGoG4/giphy.gif" class="rounded-xl shadow-2xl max-h-[60vh] object-cover" />
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">02. L'Idée avec Redmine : Un Outil Central !</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-tool-box />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Le Rôle de Redmine</span>

<div class="mr-10">

## <carbon-dashboard class="inline-block mr-2" /> Un "Chef d'Orchestre" et "Carnet de Bord"

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-data-center class="inline-block mr-2 text-orange-400" /> Il centralise toutes les infos du projet.</li>
  <li><carbon-events class="inline-block mr-2 text-orange-400" /> Il aide l'équipe à collaborer.</li>
  <li><carbon-document class="inline-block mr-2 text-orange-400" /> Il garde une trace de tout ce qui se passe.</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <img src="https://www.qsoftware.com/wp-content/uploads/2020/11/bigstock-Word-Role-Wooden-Small-Cubes-387015916-580x387.jpg" class="rounded-xl shadow-2xl max-h-[60vh] object-cover" />
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">03. Comment Ça Marche ? Gérer le Projet</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-task-complete />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Organiser le Travail</span>

<div class="mr-10">

## <carbon-folder-details class="inline-block mr-2" /> Projets et Tickets

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-application class="inline-block mr-2 text-orange-400" /> Chaque logiciel = un <strong>Projet</strong> dans Redmine.</li>
  <li><carbon-task-add class="inline-block mr-2 text-orange-400" /> Chaque tâche ou idée = un <strong>Ticket</strong>.</li>
  <li><carbon-user-avatar-filled class="inline-block mr-2 text-orange-400" /> On assigne les tickets aux bonnes personnes.</li>
  <li><carbon-progress-bar class="inline-block mr-2 text-orange-400" /> On suit leur <strong>Statut</strong> (À faire, En cours, Fini).</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <img src="https://images.unsplash.com/photo-1507925921958-8a62f3d1a50d?auto=format&fit=crop&w=600&q=80" class="rounded-xl shadow-2xl max-h-[60vh] object-cover" />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Organiser le Travail</span>

<div class="mr-10">

## <carbon-chart-line class="inline-block mr-2" /> Visualiser le Travail

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-view class="inline-block mr-2 text-orange-400" /> Voir qui fait quoi en un clin d'œil.</li>
  <li><carbon-calendar class="inline-block mr-2 text-orange-400" /> Planifier avec des plannings simples (Gantt, Calendrier).</li>
  <li><carbon-chart-multitype class="inline-block mr-2 text-orange-400" /> Savoir où en est le projet globalement.</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <div class="bg-white p-2 rounded-xl">
    <img src="https://media.istockphoto.com/id/1830042746/fr/photo/syst%C3%A8me-de-gestion-de-documents-dms-avec-des-ic%C3%B4nes-dorganisation-de-dossiers-et-de-fichiers.jpg?s=612x612&w=0&k=20&c=G3wPlq64LaaUelZLwWwOUpnmX0bVt_eYz02_8A0tJRM=" class="rounded-xl shadow-2xl max-h-[60vh] object-contain" />
  </div>
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">04. Comment Ça Marche ? Suivre les Bugs</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-debug />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Traquer les Anomalies</span>

<div class="mr-10">

## <carbon-warning-alt class="inline-block mr-2" /> Le Ticket "Bug"

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-warning class="inline-block mr-2 text-orange-400" /> Un bug est un type spécial de Ticket.</li>
  <li><carbon-document-add class="inline-block mr-2 text-orange-400" /> Quand on trouve un problème, on crée un ticket "Bug".</li>
  <li><carbon-information class="inline-block mr-2 text-orange-400" /> On y met toutes les infos pour le comprendre.</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <img src="https://media.giphy.com/media/xTiTnGeUsWOEwsGoG4/giphy.gif" class="rounded-xl shadow-2xl max-h-[60vh] object-cover" />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Traquer les Anomalies</span>

<div class="mr-10">

## <carbon-list-numbered class="inline-block mr-2" /> Infos Clés d'un Bug

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-document-blank class="inline-block mr-2 text-orange-400" /> Description précise du problème.</li>
  <li><carbon-list-numbered class="inline-block mr-2 text-orange-400" /> <strong>Les étapes pour le reproduire</strong> (très important !).</li>
  <li><carbon-user-avatar-filled class="inline-block mr-2 text-orange-400" /> Qui s'en occupe.</li>
  <li><carbon-workflow-automation class="inline-block mr-2 text-orange-400" /> Son statut (Nouveau, Corrigé, Testé...).</li>
  <li><carbon-image class="inline-block mr-2 text-orange-400" /> Possibilité d'ajouter des images (screenshots).</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <div class="bg-white p-2 rounded-xl">
    <img src="https://www.searchenginejournal.com/wp-content/uploads/2022/04/reverse-image-search-627b7e49986b0-sej.png" class="rounded-xl shadow-2xl max-h-[60vh] object-contain" />
  </div>
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">05. Redmine : Un Plus pour la Qualité Logicielle !</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-chart-evaluation />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Pourquoi Redmine aide ?</span>

<div class="mr-10">

## <carbon-improve-relevance class="inline-block mr-2" /> Visibilité et Suivi des Bugs

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-view class="inline-block mr-2 text-orange-400" /> Tout le monde voit le travail et les problèmes.</li>
  <li><carbon-checkmark-outline class="inline-block mr-2 text-orange-400" /> Aucun bug n'est oublié.</li>
  <li><carbon-progress-bar class="inline-block mr-2 text-orange-400" /> On sait toujours où on en est avec chaque problème.</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <img src="https://cdn.vectorstock.com/i/2000v/44/81/neon-sign-why-in-speech-bubble-frame-on-dark-vector-26014481.avif" class="rounded-xl shadow-2xl max-h-[60vh] object-cover" />
</div>

---
layout: two-cols
class: items-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Pourquoi Redmine aide ?</span>

<div class="mr-10">

## <carbon-time class="inline-block mr-2" /> Traçabilité Simple

<ul style="list-style-type: none;"
  class="space-y-4 text-lg mt-6"
  v-motion
  :initial="{ opacity: 0, x: -50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 200, duration: 800, stagger: 200 } }"
>
  <li><carbon-time class="inline-block mr-2 text-orange-400" /> Redmine garde l'historique de chaque ticket.</li>
  <li><carbon-user-multiple class="inline-block mr-2 text-orange-400" /> Qui a créé le bug ? Qui l'a corrigé ? Quand ?</li>
  <li><carbon-link class="inline-block mr-2 text-orange-400" /> On peut lier le bug au code qui l'a corrigé.</li>
  <li><carbon-business-metrics class="inline-block mr-2 text-orange-400" /> C'est important pour comprendre l'évolution du logiciel.</li>
</ul>

</div>

::right::

<div 
  class="pl-8 flex items-center justify-center h-full"
  v-motion
  :initial="{ opacity: 0, x: 50 }"
  :enter="{ opacity: 1, x: 0, transition: { delay: 500, duration: 800 } }"
>
  <div class="bg-white p-2 rounded-xl">
    <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80" class="rounded-xl shadow-2xl max-h-[60vh] object-contain" />
  </div>
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">06. Démonstration Pratique : Redmine en Action !</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-play />
</div>

---
layout: center
class: text-center
---

# <span class="text-2xl font-bold text-orange-400 mb-0 block">Voyons Concrètement...</span>

<div class="mt-0 text-lg max-w-3xl mx-auto">
  <ul style="list-style-type: none;"
    class="space-y-4 mt-6 text-left inline-block"
    v-motion
    :initial="{ opacity: 0, y: 50 }"
    :enter="{ opacity: 1, y: 0, transition: { delay: 200, duration: 800, stagger: 100 } }"
  >
    <li><carbon-folder-details class="inline-block text-xl text-orange-400 mr-2" /> À quoi ressemble un Projet.</li>
    <li><carbon-list-boxes class="inline-block text-xl text-orange-400 mr-2" /> La liste des Tickets (tâches et bugs).</li>
    <li><carbon-warning class="inline-block text-xl text-orange-400 mr-2" /> Les informations détaillées d'un Ticket Bug.</li>
    <li><carbon-edit class="inline-block text-xl text-orange-400 mr-2" /> Comment on peut changer le statut d'un bug.</li>
  </ul>
</div>

<div 
  class="mt-3"
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 800, duration: 800 } }"
>
  <img src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif" class="rounded-xl shadow-2xl max-h-[30vh] object-cover mx-auto" />
</div>

---
layout: section
background: https://images.pexels.com/photos/3183150/pexels-photo-3183150.jpeg
---

# <span class="text-4xl font-bold">07. Conclusion : Redmine, un Allié !</span>

<div 
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
  class="absolute bottom-10 right-10 text-5xl"
>
  <carbon-checkmark-filled />
</div>

---
layout: center
class: text-center
---

# <span class="text-3xl font-bold text-orange-400 mt-7 block">Ce Qu'il Faut Retenir</span>

<div class="text-lg max-w-3xl mx-auto">
  <ul style="list-style-type: none;"
    class="space-y-4 mt-6 text-left inline-block"
    v-motion
    :initial="{ opacity: 0, y: 50 }"
    :enter="{ opacity: 1, y: 0, transition: { delay: 200, duration: 800, stagger: 100 } }"
  >
    <li><carbon-tool-box class="inline-block text-xl text-orange-400 mr-2" /> Redmine = Outil pour organiser Projets et Tickets (Bugs inclus).</li>
    <li><carbon-view class="inline-block text-xl text-orange-400 mr-2" /> Il apporte de la <strong>visibilité</strong> et de la <strong>traçabilité</strong>.</li>
    <li><carbon-checkmark-filled class="inline-block text-xl text-orange-400 mr-2" /> Bien utiliser Redmine aide à faire des logiciels mieux organisés et avec moins de bugs.</li>
    <li><carbon-certificate class="inline-block text-xl text-orange-400 mr-2" /> C'est un outil concret au service de la <strong>Qualité Logicielle</strong>.</li>
  </ul>
</div>

<div 
  class="mt-12"
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 800, duration: 800 } }"
>
  <img src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif" class="rounded-xl shadow-2xl max-h-[30vh] object-cover mx-auto" />
</div>

---
layout: center
class: text-center
---

# <span class="text-3xl font-bold text-orange-400 mb-8 block">Merci de votre attention !</span>

<div 
  class="text-2xl text-orange-400 mt-8 mb-12"
  v-motion
  :initial="{ opacity: 0, scale: 0.8 }"
  :enter="{ opacity: 1, scale: 1, transition: { delay: 300, duration: 800 } }"
>
  Des questions ?
</div>
<carbon-help />

<div 
  class="pt-12"
  v-motion
  :initial="{ opacity: 0, y: 50 }"
  :enter="{ opacity: 1, y: 0, transition: { delay: 600, duration: 800 } }"
>
  <div class="bg-gray-800 bg-opacity-70 px-6 py-3 rounded-xl shadow-lg inline-block">
    <span class="text-xl">Présenté par André Sarr - Rachelle Ndour</span>
  </div>
</div>

<div class="abs-br m-8 flex gap-3">
  <a href="https://github.com/redmine/redmine" target="_blank" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
  <a href="https://www.redmine.org/guide" target="_blank" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-document />
  </a>
</div>

<style>
/* Ajouter ces règles globales */
img {
  object-fit: contain !important;
  max-height: 70vh;
}

.image-contain {
  background-size: contain !important;
  background-position: center center !important;
}

.grid img {
  max-height: 200px;
  width: auto !important;
}

.slidev-layout.image-right {
  grid-template-columns: 1.2fr 1fr;
  gap: 1rem;
}

/* Add styling for section slides */
.slidev-layout.section {
  @apply flex flex-col justify-center items-center;
}

.slidev-layout.section h1 {
  @apply text-sm font-bold p-4 rounded-xl bg-black bg-opacity-50 inline-block;
}

/* Supprimer les puces des listes */
ul {
  list-style: none !important;
  padding-left: 0 !important;
}


</style>
