<template>
  <div class="container">
    <div class="about-content">
      <div class="box d-flex justify-content-between align-items-center">
        <Title :badge="'ABOUT'" :text="'About Me'" />
      <a href="/assets/CV.pdf" class="d-block text-decoration-none text-light my-resume">My Resume</a>
      </div>
      <div class="detail-content">
        <img src="../../assets/img/about.png" alt="" class="w-100 h-100" />

        <div class="bio my-3 section">
          <h2 class="fw-bold">Aktamov Farrukh</h2>
          <p class="text-white-50 mb-0">Frontend Developer</p>
        </div>

        <div class="short-description section">
          <p class="text-white-50 mb-0 text-wrap">
            Proficient in frontend development with both React and Vue is a
            valuable asset to any team or project. This individual possesses a
            versatile skill set that allows to create dynamic and
            interactive user interfaces and also skilled in both React and Vue brings a
            holistic understanding of modern frontend technologies, allowing
            them to choose the right tool for the job and contribute effectively
            to the development of cutting-edge user interfaces.
          </p>
        </div>

        <div class="about-me section">
          <div class="row">
            <div class="col-lg-6 col-12">
              <ul>
                <li>
                  <b>Age: </b>
                  <span class="text-white-50 d-inline-block ms-2">23</span>
                </li>
                <li>
                  <b>Email: </b>
                  <span class="text-white-50 d-inline-block ms-2 text-wrap"
                    >farrruxaktamov677@gmail.com</span
                  >
                </li>
              </ul>
            </div>
            <div class="col-lg-6 col-12">
              <ul>
                <li>
                  <b>Nationality: </b>
                  <span class="text-white-50 d-inline-block ms-2"
                    >Uzbekistan</span
                  >
                </li>
                <li>
                  <b>Study: </b>
                  <span class="text-white-50 d-inline-block ms-2"
                    >Tashkent University of Information Technologies
                    (Graduated)</span
                  >
                </li>
                <li>
                  <b>Degree: </b>
                  <span class="text-white-50 d-inline-block ms-2"
                    >Bachelor</span
                  >
                </li>
                <li>
                  <b>Freelance: </b>
                  <span class="text-white-50 d-inline-block ms-2"
                    >Available(partly)</span
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>

        <Skills />
      </div>
    </div>
  </div>
</template>
  <script>
import "./style.css";
import { Title } from "../../ui-components";
import Skills from "../Skills/Skills.vue";
export default {
  components: {
    Title,
    Skills,
  },
};
</script>
  <style>
</style>