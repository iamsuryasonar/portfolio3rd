<template>
  <div class="footer_main">
    <p>2023 © All right Reserved</p>
    <p>Surya Sonar</p>
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
  </div>
</template>
<script>
export default {
  name: "FooterBar",
  component: {},
  data() {
    return {
      menu: false,
      linkedin: "https://www.linkedin.com/in/iamsuryasonar",
      instagram: "https://www.instagram.com/iamsuryasonar",
      github: "https://www.github.com/iamsuryasonar",
    };
  },
  methods: {},
};
</script>
<style scoped>
.footer_main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #7a86b6;
  width: 100%;
  height: 20vh;
}
.contact-icons {
  font-size: 1.6rem;
  margin-top: 1rem;
  display: flex;
  flex-direction: row;
}
.contact-icons i {
  margin: 0 1rem;
  color: white;
  cursor: pointer;
}
</style>
