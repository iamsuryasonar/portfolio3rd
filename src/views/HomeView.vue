<template>
  <NavBar> </NavBar>
  <div class="main">
    <div class="intro">
      <p>Hello World!</p>
      <p>I'm Surya Sonar</p>
    </div>
    <div class="profilepicture">
      <img src="../assets/dp.jpg" alt="a picture of Surya Sonar" />
    </div>
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
    <div class="aboutme">
      <p>
        &emsp; I am a software developer at <span><a href="https://bevyinsight.in/">Bevy Insight</a></span>, where I am dedicated to enhancing my skills in data structure and problem-solving by regularly participating in competitive programming platforms. I strive to apply the knowledge gained from these experiences to develop practical applications that benefit our clients.
      </p>
    </div>
  </div>
  <FooterBar> </FooterBar>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import FooterBar from "@/components/FooterBar.vue";
export default {
  name: "HomeView",
  components: {
    NavBar,
    FooterBar,
  },
  data() {
    return {
      linkedin: "https://www.linkedin.com/in/iamsuryasonar",
      instagram: "https://www.instagram.com/iamsuryasonar",
      github: "https://www.github.com/iamsuryasonar",
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
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  /* #191919 */
  background-color: #495c83;
  min-width: 100vw;
  min-height: 100vh;
}
.intro {
  margin-top: 4rem;
  display: grid;
  place-items: center;
}
.intro p {
  font-size: 2rem;
  padding: 0.5rem;
}

.profilepicture img {
  margin: 1.4rem auto;
  padding: 1rem;
  width: 260px;
  height: 260px;
  border-radius: 50%;
  box-shadow: 5px 15px 30px -20px rgb(3, 1, 0);
}
.contact-icons {
  font-size: 2rem;
  margin-bottom: 1rem;
  display: flex;
  flex-direction: row;
}
.contact-icons i {
  margin: 0 1rem;
  color: white;
  cursor: pointer;
}
.aboutme {
  width: 60%;
}

@media screen and (max-width: 1400px) {
  .profilepicture img {
    width: 220px;
    height: 220px;
  }
  .aboutme {
    width: 60%;
  }
}
@media screen and (max-width: 700px) {
  .profilepicture img {
    width: 180px;
    height: 180px;
  }
  .aboutme {
    width: 90%;
  }
}
</style>
