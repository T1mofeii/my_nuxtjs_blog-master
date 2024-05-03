<template>
  <div class="container-fluid home-slider">
    <div id="carouselExampleCaptions" class="carousel slide" data-ride="carousel">
      <ol class="carousel-indicators">
        <li data-target="#carouselExampleCaptions" data-slide-to="0" class="active"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="1"></li>
        <li data-target="#carouselExampleCaptions" data-slide-to="2"></li>
      </ol>
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img src="https://img.freepik.com/free-photo/3d-house-model-with-modern-architecture_23-2151004049.jpg?" class="d-block w-100" alt="Первая картинка">
          <div class="carousel-caption d-none d-md-block">
            <h5>Наша новая коллекция домов</h5>
            <p>Все эти новинки уже у нас</p>
          </div>
        </div>
        <div class="carousel-item">
          <img src="https://mykaleidoscope.ru/uploads/posts/2020-10/1602828825_2-p-dizain-eksterera-fasada-chastnogo-doma-3.jpg" class="d-block w-100" alt="Вторая картинка">
          <div class="carousel-caption d-none d-md-block">
            <h5>УЖЕ В ПРОДАЖЕ</h5>
            <p>Дома с новым дизайном</p>
          </div>
        </div>
        <div class="carousel-item">
          <img src="https://mykaleidoscope.ru/uploads/posts/2021-03/1616764596_17-p-derevyannie-doma-v-stile-modern-17.jpg" class="d-block w-100" alt="Третья картинка">
          <div class="carousel-caption d-none d-md-block">
            <h5>Уже В ПРОДАЖЕ</h5>
            <p>Дома с необычной архитектурой</p>
          </div>
        </div>
      </div>
      <a class="carousel-control-prev" href="#carouselExampleCaptions" role="button" data-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="carousel-control-next" href="#carouselExampleCaptions" role="button" data-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Slider"
}
</script>

<style scoped>

</style>
