<template>
  <div>
    <Header :h1="title"/>
    <div class="container">
    <div class="contacts">
      <h1>Контакты</h1>
      <h2>ООО «Проект жилстрой»</h2>
    </div>
    <div class="Rams">
      <div class="Rams_1">
        <p>Многоканальный телефон:</p>
        <h3>+ 7 (4913) 41-93-13</h3>
      </div>
      <div class="Rams_2">
        <p>Почта для обращения</p>
        <h3>livebild@yandex.ru</h3>
      </div>
    </div>
    <div class="Wait">
      <h2>Ждем вас в нашем офисе</h2>
      <div class="Rams2">
        <div class="Rams2_1">
          <p>Адрес:</p>
          <h3>г. Ликино-Дулево, ул. Туманова, д. 9 </h3>
        </div>
        <div class="Rams2_2">
          <p>Время работы</p>
          <h3>Вт - Сб</h3>
          <h3>10:00 - 19:00</h3>
        </div>
        <div class="Rams2_3">
          <p>Обращаем внимание</p>
          <h3>Компания «Проект Жилстрой»<br/>заключает договоры только<br/>на территории офиса.</h3>
        </div>
      </div>
    </div>
    <div class="Map">
      <h2>Карта проезда</h2>
      <!-- Компонент карты -->
      <YandexMap />
    </div>
    <div class="Consult">
      <h2>Нужна консультация?</h2>
      <p>Оставьте заявку и наши специалисты ответят на любые вопросы</p>
      <p>Или свяжитесь с нами по телефону:</p>
      <h2>+ 7 (4912) 41-92-12</h2>
      <p>г. Ликино-Дулево, ул. Туманова, д. 9 </p>
    </div>
  </div>
  </div>
</template>

<script>
import axios from "axios";
import Header from "@/components/Header";
import { required, minLength, email } from 'vuelidate/lib/validators'

export default {
  components: {Header},
  YandexMap: () => import('@/components/YandexMap.vue'),
  layout: "post_detail",
  data() {
    return {
      title: "",
      form: {
        name: '',
        email: '',
        subject: '',
        message: '',
      }
      }
    },
    methods: {
      submitForm() {
        let contactFormData = new FormData();
        contactFormData.set('name', this.form.name);
        contactFormData.set('email', this.form.email);
        contactFormData.set('subject', this.form.subject);
        contactFormData.set('message', this.form.message);
        axios({
          method: 'post',
          url: 'http://localhost:8000/api/feedback/',
          data: contactFormData
        }).then(function (response) {
          console.log(response);
        }).catch(function (response) {
          console.log(response);
        });
        this.$router.push("/success");
      }
    },
    computed: {
      isComplete () {
        return this.form.name && this.form.email && this.form.subject && this.form.message;
      }
    },
    validations: {
      form: {
        name: {
          required,
          minLength: minLength( 4 )
        },
        email: {
          email,
          required
        },
        subject: {
          required,
          minLength: minLength( 10 )
        },
        message: {
          required,
        }
      }
    },
}
  </script>

<style type="text/css">
.fld-error .msg-error  {
  display: block;
  color: #dc3545;
}
.msg-error {
  display: none;
}
</style>
