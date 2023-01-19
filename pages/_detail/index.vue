<template>
  <body>
    <main>
      <div class="recipes-detail">
        <div>
          <img
            class="recipes-detail__img"
            alt="Pasta"
            :src="$route.params.detail.recipeImage"
          />
          <h1 class="recipes-detail__title">
            {{ $route.params.detail.recipeTitle }}
          </h1>
          <p class="recipes-detail__body">
            {{ $route.params.detail.body }}
          </p>
        </div>
      </div>
    </main>
  </body>
</template>
<script>
export default {};
</script>
<style scoped>
body {
  margin: 0px;
}

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-left: 40px;
  padding-right: 40px;
  background-color: #eef2e6;
}

main {
  margin: 22px;
}

.recipes {
  display: flex;
  flex-wrap: wrap;
}

.header-nav__link {
  margin-left: 20px;
  color: black;
  text-decoration: none;
  font-size: 20px;
}
.recipes-detail {
  display: flex;
  justify-content: center;
}

.recipes-detail div {
  width: 600px;
}

.recipes-detail__img {
  width: 400px;
  height: 300px;
  display: block;
  text-align: center;
  margin: 0px auto;
}

.recipes-detail__title {
  text-align: center;
}
</style>
