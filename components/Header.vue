<template>
  <header
    class="sticky-top intro"
    style="background-color: rgba(105, 105, 105)"
  >
    <div>
      <div class="d-flex justify-content-center align-items-center h-100">
        <div class="text-white">
          <h1 class="mb-3">Название страницы</h1>
          <h5 class="mb-4 explanatory-text">Какой-то пояснительный текст</h5>
          <a
            data-mdb-ripple-init
            class="btn btn-outline-light btn-lg m-4"
            href="#"
            role="button"
            rel="nofollow"
            target="_blank"
            >О нас</a
          >
          <a
            data-mdb-ripple-init
            class="btn btn-outline-light btn-lg m-4"
            href="#"
            target="_blank"
            role="button"
            >Контакты</a
          >
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
.intro {
  height: 450px;
  box-sizing: border-box;
  padding-top: 10rem;
  margin-bottom: 10rem;
}

@media (max-width: 992px) {
  .intro {
    height: 250px;
    padding-top: 3rem;
    margin-bottom: 3rem;
  }

  .explanatory-text {
    display: none;
  }
}

@media (max-width: 650px) {
  .intro {
    height: 200px;
    padding-top: 1rem;
    margin-bottom: 2rem;
  }

  .explanatory-text {
    display: none;
  }
}
</style>
