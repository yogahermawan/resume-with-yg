<template>
  <v-row justify="center" align="center" class="bg-color">
    <v-col cols="3" class="wrapper-profile">
      <div class="circle"></div>
      <div class="profile">
        <div
          class="rounded-circle"
          elevation="12"
          style="
            overflow: hidden;
            height: 200px;
            width: 200px;
            border: 3px solid white;
          "
        >
          <v-img :src="image" alt="Yoga" />
        </div>
      </div>
      <v-list
        style="background-color: transparent; position: relative; top: -85px"
      >
        <v-list-item-group>
          <v-subheader>INFO</v-subheader>
          <v-list-item v-for="(item, i) in items" :key="i">
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
      <v-list
        style="background-color: transparent; position: relative; top: -85px"
      >
        <v-list-item-group>
          <v-subheader>SOCIALS</v-subheader>
          <v-list-item v-for="(item, i) in socials" :key="i">
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-col>
    <v-col>
      <ul>
        <li>
          Hai, saya Yoga Hermawan seorang Software Engineer dengan pengalaman
          kurang lebih 4 th. Minat saya adalah tentang pembuatan atau
          pengembangan sebuah aplikasi, saya juga sangat tertarik untuk menjadi
          product manager.
        </li>
      </ul>
    </v-col>
  </v-row>
</template>

<script>
import Mail from "~/components/icons/Mail.vue";
import Home from "~/components/icons/Home.vue";
import Phone from "~/components/icons/Phone.vue";
export default {
  name: "IndexPage",
  components: {
    Mail,
    Home,
    Phone,
  },
  data() {
    return {
      image: "/img/yg.jpg",
      items: [
        {
          text: "DI. Yogyakarta",
          icon: "mdi-home",
        },
        { text: "085802672801", icon: "mdi-phone" },
        { text: "yogahermawan43@gmail.com", icon: "mdi-gmail" },
      ],
      socials: [
        {
          text: "url",
          icon: "mdi-github",
        },
        { text: "yogahermawan", icon: "mdi-linkedin" },
        { text: "@_yogahermawan", icon: "mdi-instagram" },
      ],
    };
  },
  methods: {
    home() {
      return `<Home />`;
    },
    phone() {
      return `<Phone />`;
    },
  },
};
</script>

<style scoped>
.bg-color {
  background-color: #b8fff9;
}
.wrapper-profile {
  position: relative;
  background-color: #82dbd8;
  height: 100vh;
  padding: 0;
}
.circle {
  background-color: #42c2ff;
  height: 150px;
  width: 100%;
  position: relative;
  left: 0;
  top: -35px;
  transform: skewY(-10deg);
}
.profile {
  display: flex;
  justify-content: center;
  top: -115px;
  position: relative;
}
@media only screen and (min-width: 1264px) {
  .container {
    max-width: 1260px !important;
  }
}
</style>