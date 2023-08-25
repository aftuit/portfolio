<template>
    <div class="portfolio-card w-100 p-1">
        <a :href="site.link" target="_blank" class="text-decoration-none text-white">
            <div class="card p-0 bg-dark-50">
                <div class="card-header p-0">
                    <img :src="site.image" alt="" class="w-100 h-100 card-image">
                </div>
                <div class="visit"><i class="fa-sharp fa-solid fa-arrow-up" style="color: #fff;"></i></div>

                <div class="card-body">
                    <h4 class="card-title text-center text-decoration-none ">{{ site.title }}</h4>
                    <div class="stacks">
                        <span v-for="stack in site.stacks" :key="stack" class="badge badge-light bg-light text-dark mx-1 fw-normal">{{stack}}</span>
                    </div>
                </div>
            </div>
        </a>
    </div>
</template>
<script>
import "./style.css"
export default {
    props: {
        site : {
            type: Object,
            required: true
        }
    }
}
</script>
<style>
    
</style>