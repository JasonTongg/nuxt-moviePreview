<template>
  <body>
    <main>
      <div class="recipes">
        <div class="recipes-content" v-for="recipe in recipes" :key="recipe.id">
          <img
            class="recipes-content__img"
            alt="Pasta"
            :src="recipe.recipeImage"
          />
          <div class="recipes-content__body">
            <nuxt-link
              tag="h1"
              class="recipes-content__body__title"
              :to="{ name: 'detail', params: { detail: recipe } }"
            >
              {{ recipe.recipeTitle }}
            </nuxt-link>
            <div class="recipes-content__body__review">
              <img src="images/heart.png" alt="Heart" />
              <p>{{ recipe.likes }} likes</p>
            </div>
          </div>
        </div>
      </div>
    </main>
    <footer></footer>
  </body>
</template>

<script>
export default {
  name: "IndexPage",
  data() {
    return {
      recipes: [
        {
          id: 1,
          recipeImage: "https://i.ibb.co/SBsMYNC/Rendang.jpg",
          recipeTitle: "Rendang",
          likes: 100,
          body: "Rendang Recipe",
        },
        {
          id: 2,
          recipeImage: "https://i.ibb.co/MRNhgzW/Tomyam.jpg",
          recipeTitle: "Tomyam",
          likes: 40,
          body: "Tomyam Recipe",
        },
        {
          id: 3,
          recipeImage: "https://i.ibb.co/CW4tVvp/Spaghetti-aglioo-o-lio.jpg",
          recipeTitle: "Spagethi Aglio Olio",
          likes: 200,
          body: "Spagethi Aglio Olio Recipe",
        },
        {
          id: 4,
          recipeImage: "https://i.ibb.co/z7zRVxV/Spaghetti-Carbonara.jpg",
          recipeTitle: "Spagethi Carbonara",
          likes: 200,
          body: "Spagethi Carbonara Recipe",
        },
        {
          id: 5,
          recipeImage: "https://i.ibb.co/Cn1XPNB/Kimchi.jpg",
          recipeTitle: "Kimchi",
          likes: 10,
          body: "Kimchi Recipe",
        },
      ],
    };
  },
};
</script>
<style scoped>
.recipes {
  display: flex;
  flex-wrap: wrap;
}
.recipes-content {
  background-color: #eef2e6;
  padding: 10px;
  margin: 13px 13px;
}

.recipes-content__body {
  padding: 5px;
}

.recipes-content__img {
  width: 280px;
  height: 210px;
}

.recipes-content__body__review {
  display: flex;
  align-items: center;
}
.recipes-content__body__review img {
  width: 20px;
  height: 20px;
  margin: 5px 10px 5px 0px;
}

.recipes-content__body__review p {
  margin: 0px;
}

.recipes-content__body__review img:hover {
  cursor: pointer;
}

.recipes-content__body__title {
  margin: 5px 0px;
}
</style>
