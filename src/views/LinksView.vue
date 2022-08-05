<template>
  <NavBar> </NavBar>
  <div class="main">
    <div class="wrapper">
      <h1>Links</h1>
      <div class="contact-icons">
        <a class="iconcontact" :href="linkedin">
          <i class="fab fa-linkedin"></i>
        </a>
        <a class="iconcontact" :href="instagram">
          <i class="fab fa-instagram"></i>
        </a>
        <a class="iconcontact" :href="github">
          <i class="fab fa-github"></i>
        </a>
      </div>
      <div class="link_cards">
        <a
          :href="link.url"
          class="link_card"
          v-for="(link, id) in links"
          :key="id"
        >
          <p class="link_title">{{ link.title }}</p>
        </a>
      </div>
    </div>
  </div>
  <FooterBar> </FooterBar>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import FooterBar from "@/components/FooterBar.vue";
export default {
  name: "LinksView",
  components: {
    NavBar,
    FooterBar,
  },
  data() {
    return {
      links: [
        {
          id: "URLshare",
          title: "URLshare - a link sharing platform",
          url: "https://urlshare.netlify.app",
        },
        {
          id: "resume",
          title: "My Resume - updated on 15-May-2022",
          url: "https://drive.google.com/file/d/13xR78QwjFNJzhtQ2hQru6aK0DxCEuNQE/view?usp=sharing",
        },
      ],
    };
  },
};
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  color: white;
}
body {
  overflow-x: hidden;
}
.main {
  background-color: #495c83;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.wrapper {
  margin-top: 5rem;
  margin-bottom: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 100vw;
  min-height: 90vh;
}
.contact-icons {
  font-size: 2rem;
  margin-top: 3vh;
  display: flex;
  flex-direction: row;
}
.contact-icons i {
  margin: 0 1rem;
  color: white;
  cursor: pointer;
}
.link_cards {
  margin: 1rem 1rem;
  width: 60%;
}
.link_card {
  margin: 1rem 1rem;
  /* width: 60%; */
  height: 5rem;
  background-color: #7a86b6;
  display: flex;
  justify-content: center;
  align-items: center;
}
a {
  color: white;
  text-decoration-line: none;
}

@media screen and (max-width: 1400px) {
  .link_card {
    margin: 0.6rem 0.6rem;
  }
  .link_cards {
    width: 60%;
  }
}
@media screen and (max-width: 700px) {
  .link_card {
    margin: 1.2rem 0.4rem;
  }
  .link_cards {
    width: 90%;
  }
}
</style>
