<template>
    <div class="portfolio">
        <h1>Showing My Work</h1>
        <h5>Examples of my projects, that I would be more than happy to talk about more in depth!</h5>
        <div class="experience" v-for="work in works" :key="work.name">
            <h3>{{work.name}}</h3>
            <a :href="work.url" target="_blank">{{work.url}}</a>
        </div>
    </div>
</template>

<script>
export default {
    name: 'PortfolioInfo',
    data : function(){
        return{
            works : [
                { name : "This Website!", url : "https://github.com/JFoxx64/dsresume" },
                { name : "Scam Takedown Task Force Plugin", url : "https://github.com/JFoxx64/scamtdtf-site-scanner" },
                { name : "Scam Takedown Task Force Website", url : "https://scamtdtf.com" },
                { name : "Dan's Tech Services", url : "https://danstechservices.us" },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.portfolio{
    width: 80%;
    margin: auto;
    padding-bottom: 50px;
}
a {
    color: #32b3b8;
}
a:active{
    color: #3edbe0;
}
</style>
