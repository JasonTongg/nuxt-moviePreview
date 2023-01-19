<template>
  <body>
    <main>
      <div class="add-recipe">
        <label>
          <b>Image Link : </b>
          <input
            type="text"
            placeholder="https://www.image.com/..."
            class="add-recipe__img"
          />
        </label>
        <input type="text" placeholder="Title ..." class="add-recipe__title" />
        <hr />
        <textarea
          placeholder="Your Recipe ....."
          class="add-recipe__desc"
        ></textarea>
        <button class="add-recipe__button">Add Recipe</button>
      </div>
    </main>
  </body>
</template>
<script>
export default {};
</script>
<style scoped>
.add-recipe__title,
.add-recipe__desc {
  display: block;
  width: 100%;
  margin: 10px 0px;
  border: none;
}

.add-recipe__title {
  height: 50px;
  font-size: 25px;
}

.add-recipe__desc {
  height: 300px;
}

.add-recipe__img {
  border: none;
  height: 30px;
}

.add-recipe__button {
  color: white;
  background-color: #4b56d2;
  border: none;
  padding: 20px;
  border-radius: 15px;
  font-weight: bold;
}

.add-recipe__button:hover {
  cursor: pointer;
  background-color: #82c3ec;
  color: #4b56d2;
}
</style>
