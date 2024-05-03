<template>
  <div class="container">
    <div class="Footer_block">
      <div class="footer_price-list">
        <h1>Прайс-лист</h1><nuxt-link class="nav-link" to="/" style="color: #750000; margin-top: 50px">Прайс-лист</nuxt-link>
      </div>
      <div class="footer_contacts">
        <h1>Контакты</h1><nuxt-link class="nav-link" to="/contact" style="color: #750000; margin-top: 50px">Контакты</nuxt-link>
      </div>
    </div>
    <div class="footer_info">
      <div class="logo"><img src="https://github.com/T1mofeii/Practica/blob/master/src/styles/img/image1.png?raw=true" alt="logo"/></div>
      <p>© Проект жилстрой, 2009 — 2023. Все материалы данного сайта являются объектами авторского права (в том числе дизайн). Запрещается копирование, распространение<br/>(в том числе путём копирования на другие сайты и ресурсы в Интернете) или любое иное использование информации и объектов без предварительного согласия<br/>правообладателя. Cайт не является публичной офертой. Строительная компания «Проект жилстрой» оставляет за собой право изменять цены и условия специальных<br/>предложений без предварительного уведомления. </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  props: ['username']
}
</script>

<style scoped>

</style>
