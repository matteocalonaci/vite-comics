<!-- JS -->
<script>
import ComicsList from "./ComicsList.vue";
export default {
  components: {
    ComicsList
  },
  name: "AppMain",
  data() {
    return {
      fumetti: [
        {
          thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
        }
      ]
    }
  }
}
</script>

<!-- HTML -->
<template>
  <main>
    <div class="jumbotron">
      <img src="../assets/jumbotron.jpg" alt="">
    </div>
    <div class="container">
      <div class="col-12 text-center">
        <h2 class="p-2 my-bg text-white"><b>CURRENT SERIES</b></h2>
      </div>

      <div class="row">
        <div class="col-12">
          <div class="row p-4 d-flex justify-content-center"> <!-- Added Bootstrap classes here -->
            <ComicsList v-for="card in fumetti" :key="card.series" :fumetti="card" />
          </div>
        </div>
      </div>
      <div class="p-5">
      <button class="d-flex m-auto">LOAD MORE</button>
      </div>
    </div>
  </main>
</template>


<!-- CSS -->
<style scoped>
main {
height: auto;  background: #222;
}

.jumbotron {
  height: 20rem;
  position: relative;
}

h2 {
  margin: 1rem 0; 
}

img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  object-position: top;
}

button {
  background-color: rgb(2, 130, 249);
  border: 0.1rem solid rgb(2, 130, 249);
  color: white;
  padding: 0.5rem 2rem;
  text-align: center;
}

.my-bg {
  background-color: rgb(2, 130, 249);
}

.card {
  margin: 1rem; 
  display: flex; 
  flex-direction: column; 
  align-items: center; 
  width:  calc((100% - 2rem) /5);
}

.card img {
  height: 17rem;
  width: 100%;
  object-fit: cover;
}

@media (max-width: 768px) {
  .col-12 {
    height: auto; 
  }

  h2 {
    margin-top: 2rem; 
  }

  .card {
  margin: 1rem;
  display: flex; 
  flex-direction: column; 
  align-items: center; 
  width:  calc((100% - 2rem)/1);
}

}
</style>