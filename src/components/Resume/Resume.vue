<template>
  <div class="resume-content">
    <div class="container ">
      <div class="row resume-row bg-dark-50">
        <div class="col-xl-6 col-12">
          <div class="left">
            <div class="section-title">
              <h3>Education</h3>
            </div>
            <div class="resume-list">
              <ul>
                <li v-for="edu in education" :key="edu.id">
                  <div class="list_inner">
                    <div class="time">
                      <span>{{ edu.year }}</span>
                    </div>
                    <div class="place">
                      <h3>{{ edu.place }}</h3>
                      <span class="text-white-50">{{ edu.degree }}</span>
                    </div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
        <div class="col-xl-6 col-12">
          <div class="right">
            <div class="section-title">
              <h3>Experience</h3>
            </div>
            <div class="resume-list">
              <ul>
                <li v-for="edu in experience" :key="edu.id">
                  <div class="list_inner">
                    <div class="time">
                      <span>{{ edu.year }}</span>
                    </div>
                    <div class="place">
                      <h3>{{ edu.place }}</h3>
                      <span class="text-white-50">{{ edu.degree }}</span>
                    </div>
                  </div>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
  <script>
import "./style.css";
import { Title } from "../../ui-components";
export default {
  data() {
    return {
      education: [
        {
          id: 1,
          year: '2016 - 2019',
          place: 'College of information technologies',
          degree: 'High-school'
        },
        {
          id: 2,
          year: '2019 - 2023',
          place: 'Tashkent University of Information Technologies (Graduated)',
          degree: 'Bachelor Degree'
        },
        {
          id: 3,
          year: '2006 - 2023',
          place: 'Elementery school',
          degree: ''
        },
      ],
      experience: [
        {
          id: 4,
          year: '06/2021 - 08/2021',
          place: 'Algorithm Consulting Group',
          degree: 'JavaScript Developer (Intern)'
        },
        {
          id: 5,
          year: '01/2022 - 08/2022',
          place: 'Online',
          degree: 'Freelance (partly)'
        },
        {
          id: 6,
          year: '09/2022 - 12/2022',
          place: 'Zako IT Academy',
          degree: 'React Developer'
        },
        {
          id: 7,
          year: '01/2023 - now',
          place: 'Online',
          degree: 'React / Vue Freelance (partly)'
        },
      ]
    }
  },
  components: {
    Title,
  },
};
</script>
  <style>
</style>