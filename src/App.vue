<template>
  <v-app id="inspire">
    <!--  https://vuetifyjs.com/en/components/app-bars/#toggle-navigation-drawers  -->
    <v-app-bar
        app
        color="white"
        elevate-on-scroll
        shrink-on-scroll
    >
      <v-container class="py-0 fill-height" fluid>
        <!--  io logo here  -->
        <v-row>
          <v-col class="justify-end" cols="6">
            <v-img
                class="nav-img"
                contain
                max-height="150"
                max-width="150"
                src="../src/assets/logo.svg"
            ></v-img>
          </v-col>

          <v-col cols="6">
            <v-spacer></v-spacer>
            <v-btn
                v-for="link in links"
                :key="link"
                text
            >
              {{ link }}
            </v-btn>
            <v-btn
                color="#7683F7"
                large
                rounded
                width="220px"
            >
              Увійти
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </v-app-bar>

    <v-main class="io">
      <v-container fluid>
        <v-row align="center" justify="center">
          <v-col cols="6">
            <v-container class="io-container">
              <h2 class="io-header">
                Система Інвентаризації
              </h2>
              <p class="io-para">IO — це система інвентаризації розроблена для ведення електронного обліку обладнання
                та ліцензій програмного забезпечення на підприємстві.
              </p>
              <v-btn
                  color="#7683F7"
                  large
                  rounded
                  width="220px"
              >
                Увійти
              </v-btn>
            </v-container>
          </v-col>
          <v-col cols="6">
            <v-img contain height="812px" src="../src/assets/QR 1.svg"></v-img>
          </v-col>
        </v-row>
      </v-container>
      <v-container class="io-problems-container pa-16" fluid>
        <v-row class="fill-height" justify="center">
          <h3 class="io-problems">Робота з нами</h3>
        </v-row>
      </v-container>
      <v-container class="pa-16" fluid>
        <v-row align="center" class="fill-height pa-16" justify="center">
          <v-img src="../src/assets/Group 132.svg"></v-img>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
          <v-col cols="1.5">
            <p>This is some text</p>
          </v-col>
        </v-row>
      </v-container>
      <v-container class="io-problems-container pa-16" fluid>
        <v-row class="fill-height" justify="center">
          <h3 class="io-problems">Проблеми</h3>
        </v-row>
      </v-container>
      <div>
        <template>
          <v-parallax height="300" src="../src/assets/image.png">
            <v-overlay absolute color="#4354F2" opacity="0.5" value="true"><p
                class="text-center io-parallax-paragraph pa-16">Система дозволяє зберігання інформації про
              обладнання та програмне забезпечення, збереження історії про
              ремонти, передачі, списання та утилізації обладнання, формування звітів. Не потребує встановлення на
              персональний комп’ютер.</p>
            </v-overlay>
          </v-parallax>
        </template>
      </div>
      <v-container class="io-problems-container pa-16" fluid>
        <v-row class="fill-height" justify="center">
          <h3 class="io-problems">Переваги</h3>
        </v-row>
        <v-row justify="center">
          <v-col cols="2">
            <template>
              <v-hover v-slot:default="{ hover }">
                <v-card
                    :elevation="hover ? 20 : 4"
                    class="mx-auto my-12 elevation-15 card text-center rounded-card"
                    height="300"
                    max-width="374"
                    transition="scale-transition"
                >
                  <v-container class="pa-5">
                    <v-icon class="pa-10" x-large>mdi-google
                      <v-img src="../src/assets/Ellipse 11.svg"></v-img>
                    </v-icon>
                    <p class="justify-center pa-3">
                      Легкий перегляд пов’язаної інформації у одному місці
                    </p>
                  </v-container>
                </v-card>
              </v-hover>
            </template>
          </v-col>
          <v-col cols="2">
            <template>
              <v-hover v-slot:default="{ hover }">
                <v-card
                    :elevation="hover ? 20 : 4"
                    class="mx-auto my-12 elevation-15 card text-center rounded-card"
                    height="300"
                    max-width="374"
                >
                  <v-container class="pa-5">
                    <v-icon class="pa-10" x-large>mdi-google
                      <v-img src="../src/assets/Ellipse 11.svg"></v-img>
                    </v-icon>
                    <p class="justify-center pa-3">
                      Простий інтерфейс у стилі material design
                    </p>
                  </v-container>
                </v-card>
              </v-hover>
            </template>
          </v-col>
          <v-col cols="2">
            <template>
              <v-hover v-slot:default="{ hover }">
                <v-card
                    :elevation="hover ? 20 : 4"
                    class="mx-auto my-12 elevation-15 card text-center rounded-card"
                    height="300"
                    max-width="374"
                >
                  <v-container class="pa-5">
                    <v-icon class="pa-10" x-large>mdi-google
                      <v-img src="../src/assets/Ellipse 11.svg"></v-img>
                    </v-icon>
                    <p class="justify-center pa-3">
                      Швидка авторизація через Google OAuth 2.0
                    </p>
                  </v-container>
                </v-card>
              </v-hover>
            </template>
          </v-col>
          <v-col cols="2">
            <template>
              <v-hover v-slot:default="{ hover }">
                <v-card
                    :elevation="hover ? 20 : 4"
                    class="mx-auto my-12 elevation-15 card text-center rounded-card"
                    height="300"
                    max-width="374"
                >
                  <v-container class="pa-5">
                    <v-icon class="pa-10" x-large>mdi-google
                      <v-img src="../src/assets/Ellipse 11.svg"></v-img>
                    </v-icon>
                    <p class="justify-center pa-3">
                      Доступ з будь-якого сучасного веб-браузера
                    </p>
                  </v-container>
                </v-card>
              </v-hover>
            </template>
          </v-col>
          <v-col cols="2">
            <template>
              <v-hover v-slot:default="{ hover }">
                <v-card
                    :elevation="hover ? 20 : 4"
                    class="mx-auto my-12 elevation-15 card text-center rounded-card"
                    height="300"
                    max-width="374"
                >
                  <v-container class="pa-5">
                    <v-icon class="pa-10" x-large>mdi-google
                      <v-img src="../src/assets/Ellipse 11.svg"></v-img>
                    </v-icon>
                    <p class="justify-center pa-3">
                      Інтеграція з Google Workspace
                    </p>
                  </v-container>
                </v-card>
              </v-hover>
            </template>
          </v-col>
        </v-row>
      </v-container>
      <v-container class="io-problems-container pa-16" fluid>
        <v-row class="fill-height" justify="center">
          <v-col cols="6" class="justify-center">

          </v-col>
          <v-col cols="4" class="justify-center">
            <h3 class="io-problems">Отримати доступ</h3>
            <v-text-field
                v-model="fullname"
                clearable
                color="purple"
                label="ПІБ"
            ></v-text-field>
            <v-text-field
                v-model="organizationName"
                clearable
                color="purple"
                label="Назва організації"
            ></v-text-field>
            <v-text-field
                v-model="email"
                clearable
                color="purple"
                label="Email"
            ></v-text-field>
            <v-text-field
                v-model="phone"
                clearable
                color="purple"
                label="Номер телефону"
            ></v-text-field>
            <v-textarea
                v-model="msg"
                clearable
                color="purple"
            >
              <template v-slot:label>
                <div>
                  Повідомлення
                </div>
              </template>
            </v-textarea>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import '../src/assets/styles/style.css';

export default {
  data: () => ({
    links: [
      'Робота з нами',
      'Проблеми',
      'Переваги',
      'Команда',
    ],
    fullname: '',
    organizationName: '',
    email: '',
    phone: '',
    msg: '',
  }),
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Nunito&display=swap');

* {
  font-family: 'Nunito', sans-serif !important;
}

.title {
  font-family: 'Nunito', sans-serif !important;
}

.v-btn__content {
  font-size: 18px;
}

.nav-img {
  margin-left: 10vw;
}

.io {
  background-color: rgba(217, 220, 245, 0.5);
}

.rounded-card {
  border-radius: 15px !important;
}

.rounded.v-image__image.zoom.v-image__image {
  transition: all 0.2s;
  transform: scale(1.2);
}

.io-container {
  margin-left: 15vw;
}

.io-header {
  font-style: normal;
  font-weight: bold;
  font-size: 42px;
  line-height: 57px;
}

#io-shape {
  background: url('../src/assets/BgShape.svg') no-repeat center center fixed !important;
  height: 1000px;
  width: 100px;
  z-index: -1;
}

.io-problems {
  font-family: Nunito;
  font-style: normal;
  font-weight: normal;
  font-size: 48px;
  line-height: 65px;
}

.io-problems-container {
  background-color: white;
}

.io-para {
  font-family: Nunito;
  font-style: normal;
  font-weight: normal;
  width: 830px;
  font-size: 36px;
  line-height: 49px;
}

.io-login {
  width: 220px;
  height: 50px;
  left: 248px;
  top: 603px;
}

.io-second {
  background: url('../src/assets/Group 132.svg') no-repeat center center fixed !important;
  background-size: cover;
  background-color: red;
}

.io-parallax-paragraph {
  font-weight: 900;
  font-size: 22px;
  line-height: 30px;
}
</style>
