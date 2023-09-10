<template>
    <div class="skills">
        <div class="section mb-0">
            <div class="row">
                <div class="col-md-6 col-12">
                    <h3 class="skill-title">Knowledge</h3>
                    <ul class="mt-4">
                        <li v-for="skill in skills" :key="skill">
                            <i class="fa-solid fa-caret-right fa-sm" style="color: #000000;"></i>
                            <span class="text-white-50 d-inline-block ms-2">{{ skill }}</span>
                        </li>
                    </ul>
                    
                </div>
                <div class="col-md-6 col-12">
                    <h3 class="skill-title">Languages</h3>
                    <ul class="mt-4">
                        <li v-for="language in languages" :key="language">
                            <i class="fa-solid fa-caret-right fa-sm" style="color: #000000;"></i>
                            <span class="text-white-50 d-inline-block ms-2">{{ language }}</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import "./style.css"
export default {
    data() {
        return {
            skills: [
                'Javascript',
                'Typescript (basic)',
                'React (Redux, NextJS)',
                'Vue (Vuex, Pinia)',
                'Tailwind Css',
                'Styled Components',
                'Git',
            ],
            languages: [
                'Uzbek (native)',
                'English (IELTS 6)',
                'Russian (elementary proficiency)'
            ]
        }
    }
}
</script>
<style>
    
</style>