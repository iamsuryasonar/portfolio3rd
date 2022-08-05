<template>
  <NavBar> </NavBar>
  <div class="main">
    <div class="wrapper">
      <h1>Skills</h1>
      <p>
        These are some languages,frameworks and tools that I have experience
        with.
      </p>
      <div class="skill_grid">
        <ul class="skill_card">
          <li v-for="(skill, id) in skills" :key="id">
            <img class="skill_icon" v-bind:src="skill.image" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </div>
  <FooterBar> </FooterBar>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import FooterBar from "@/components/FooterBar.vue";
import git from "@/assets/dev_icons/git.svg";
import android from "@/assets/dev_icons/android.svg";
import css3 from "@/assets/dev_icons/css3.svg";
import dart from "@/assets/dev_icons/dart.svg";
import firebase from "@/assets/dev_icons/firebase.svg";
import figma from "@/assets/dev_icons/figma.svg";
import flutter from "@/assets/dev_icons/flutter.svg";
import github from "@/assets/dev_icons/github.svg";
import nodejs from "@/assets/dev_icons/nodejs.svg";
import javascript from "@/assets/dev_icons/javascript.svg";
import java from "@/assets/dev_icons/java.svg";
import html5 from "@/assets/dev_icons/html5.svg";
import vuejs from "@/assets/dev_icons/vuejs.svg";
import vscode from "@/assets/dev_icons/vscode.svg";
export default {
  name: "SkillsView",
  components: {
    NavBar,
    FooterBar,
  },
  data() {
    return {
      skills: [
        {
          id: "git",
          image: git,
        },
        {
          id: "android",
          image: android,
        },
        {
          id: "flutter",
          image: flutter,
        },
        {
          id: "firebase",
          image: firebase,
        },
        {
          id: "javascript",
          image: javascript,
        },
        {
          id: "java",
          image: java,
        },
        {
          id: "nodejs",
          image: nodejs,
        },
        {
          id: "vscode",
          image: vscode,
        },
        {
          id: "vuejs",
          image: vuejs,
        },
        {
          id: "html5",
          image: html5,
        },
        {
          id: "github",
          image: github,
        },
        {
          id: "css3",
          image: css3,
        },
        {
          id: "dart",
          image: dart,
        },
        {
          id: "figma",
          image: figma,
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
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #495c83;
  min-width: 100vw;
  min-height: 100vh;
}
.wrapper {
  margin-bottom: 2rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-width: 100vw;
  min-height: 100vh;
}
.wrapper p {
  margin-top: 1rem;
  width: 60%;
}
.skill_grid {
  margin-top: 1rem;
}
.skill_card {
  list-style: none;
  margin: auto;
  text-align: left;
  width: 60%;
}
.skill_card li {
  /* background-color: #787878; */
  display: inline-block;
  /* margin: 0.4rem; */
  padding: 0.8rem 1.2rem;
}

.skill_icon {
  height: 60px;
  width: 60px;
}
@media screen and (max-width: 1400px) {
  .main p {
    width: 70%;
  }
  .skill_card {
    width: 70%;
  }
}
@media screen and (max-width: 700px) {
  .main p {
    width: 90%;
  }
  .skill_card {
    width: 90%;
  }
  .skill_card li {
    margin: 0.2rem;
    padding: 0.4rem 0.8rem;
  }
}
</style>
