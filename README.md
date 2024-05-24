# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Vue - Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (previously Volar) and disable Vetur


----------------------------------GIOTNO 1-------------------------------------

MILESTONE 1
Create un nuovo progetto utilizzando Vite e Vue 3.
Definite i componenti necessari per strutturare il layout come da screenshot allegato.
Dovrete avere almeno tre componenti: AppHeader, AppMain e AppFooter.
Aiutatevi guardando il codice del live coding di ieri e di oggi e soprattutto controllando cosa cambia tra le varie commit.



MILESTONE 2
Realizzate una struttura a blocchi colorati, come abbiamo fatto in passato per layout lunghi come discord o dropbox.
Quando la struttura è pronta fate in modo di scrivere le voci di menu nel relativo componente, usando i data e un v-for.
Per oggi diamo priorità alla struttura: solo quando è tutto bello solido, passiamo allo style! :avviso:
L'obiettivo principale è imparare a muoversi tra i componenti, non realizzare una pagina "bella".


----------------------------------GIOTNO 2-------------------------------------

CONSEGNA
Continuate a lavorare nella stessa repo di ieri. Oggi però andiamo a popolare il main content.

 MILESTONE 1
Create un componente che in base ad un array (in allegato) vada a generare delle card in pagina.
Sarà il macro componente che contiene tutti i fumetti, qualcosa come ComicsList.vue.
Dovrete copiare l'array allegato nel vostro data e iterare con un v-for.

MILESTONE 2
Ora provate a creare un componente figlio che rappresenti la singola card, del tipo SingleComic.vue.
Fate in modo che accetti un dato in ingresso (usando le props).
Dal componente padre (es. ComicsList) modificate il ciclo in modo che richiami questo nuovo componente e gli passi il fumetto in questione tramite props.
