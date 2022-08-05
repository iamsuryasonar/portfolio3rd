<template>
  <nav id="navbar">
    <div class="nav-wrapper">
      <div class="namediv">
        <a href="/">
          <p @click="menu = false" class="name">Surya Sonar</p>
        </a>
      </div>

      <div class="about-project-contact">
        <a href="/"><p class="about">About Me</p></a>
        <a href="/projects">
          <p class="projects">Projects</p>
        </a>
        <a href="/skills">
          <p class="skills">Skills</p>
        </a>
        <a href="/links">
          <p class="links">Links</p>
        </a>
      </div>
      <div class="menuiconwrapper" @click="menu = !menu">
        <div class="barsicon" v-if="!menu">
          <i id="menuopenbutton" class="fas fa-bars"></i>
        </div>
        <div class="barsicon" v-if="menu">
          <i id="menuclosebutton" class="fas fa-times"></i>
        </div>
      </div>
    </div>
  </nav>
  <div class="menuoverlay" v-if="menu">
    <div class="menuoverlaywrapper">
      <div class="menucontents">
        <a href="/">
          <p @click="menu = !menu" id="about">About Me</p>
        </a>
        <a href="/projects">
          <p @click="menu = !menu">Projects</p>
        </a>
        <a href="/skills">
          <p @click="menu = !menu">Skills</p>
        </a>
        <a href="/links">
          <p @click="menu = !menu">Links</p>
        </a>
      </div>
      <div class="menusocialicons">
        <a :href="linkedin">
          <i @click="menu = !menu" class="fab fa-linkedin"></i
        ></a>
        <a :href="instagram">
          <i @click="menu = !menu" class="fab fa-instagram"></i
        ></a>
        <a :href="github">
          <i @click="menu = !menu" class="fab fa-github"></i
        ></a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "NavBar",
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
#navbar {
  background-color: #7a86b6;
  position: fixed;
  width: 100%;
  z-index: 222;
}

#navbar .nav-wrapper {
  height: 8vh;
  width: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  margin: 1rem 2rem;
}
#navbar p {
  cursor: pointer;
  font-size: 1.4rem;
  font-weight: 300;
  color: #ffffff;
}
#navbar .name {
  font-family: "Montserrat", sans-serif;
  font-size: 2rem;
  color: #ffffff;
}
.namediv a {
  text-decoration: none;
}
/* <-----------menu button and overlay--------------> */
#navbar .name:hover {
  color: #abf0ef;
}
.menuiconwrapper {
  display: none;
}
#menuclosebutton,
#menuopenbutton {
  cursor: pointer;
  font-size: 2.2rem;
  color: #ffffff;
}
#menuclosebutton:hover,
#menuopenbutton:hover {
  color: #5bbdbc;
}
.menuoverlay {
  position: fixed;
  height: 350px;
  width: 100vw;
  background-color: #7a86b6;
  z-index: 99;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.menuoverlaywrapper {
  width: 70%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.menucontents {
  margin-top: 2rem;
}
.menucontents a,
.menusocialicons a {
  text-decoration: none;
  color: white;
}
.menucontents a:hover,
.menusocialicons a:hover {
  color: #5bbdbc;
}
.menucontents p {
  cursor: pointer;
  margin: 1rem auto;
  text-align: center;
}
.menucontents p:hover {
  border-bottom: 2px solid #e4e403;
}
.menucontents,
.menusocialicons {
  font-size: 1.4rem;
  color: white;
}
.menusocialicons i {
  cursor: pointer;
  margin: 1rem 1rem;
}
.menusocialicons i:hover {
  color: #5bbdbc;
}
/* <----------------------------------------------------> */
.about-project-contact {
  width: 40%;
  margin-right: 3rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.about-project-contact a {
  text-decoration: none;
}

.about-project-contact p:hover {
  border-bottom: 2px solid #e4e403;
}

/* 700px and above */
@media screen and (min-width: 900px) {
  .menuoverlay {
    display: none;
  }
}
/* 1020px and below */
@media screen and (max-width: 1020px) {
  .about-project-contact {
    width: 50%;
  }
}
/* 700px and below */
@media screen and (max-width: 900px) {
  .menuiconwrapper {
    display: block;
  }
  #navbar .name {
    font-size: 1.6rem;
  }
  #menuopenbutton,
  #menuclosebutton {
    font-size: 1.4rem;
  }
  .about-project-contact {
    display: none;
  }
}
</style>
