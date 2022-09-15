<template>
    <div class="skillset">
        <h1>Skills</h1>
        <h5>Skills that I feel comfortable with in some capacity - some of them more than others but always looking to grow!</h5>
        <input type="text" v-model="skillsearch" placeholder = "Search for one you're looking for">
        <div class = "skills">
            <div class="skill" v-for="skill in skills" :key="skill.name" :class="{ hidden : (!skill.name.toLowerCase().includes(skillsearch.toLowerCase()) && !skillsearch == '') }">
                <h3>{{skill.name}}</h3>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SkillSet',
    data : function(){
        return{
            skills : [
                { name : "JavaScript",  weight : 0 },
                { name : "MySQL",       weight : 0 },
                { name : "NodeJS",      weight : 0 },
                { name : "HTML5",       weight : 0 },
                { name : "CSS",         weight : 0 },
                { name : "Vue.js",      weight : 0 },
                { name : "C#",          weight : 0 },
                { name : "Java",        weight : 0 },
                { name : "Angular 2+",  weight : 0 },
                { name : "Python",      weight : 0 },
                { name : "C",           weight : 0 },
                { name : "Windows OS",  weight : 0 },
                { name : "Linux",       weight : 0 },
                { name : "Rasbian OS",  weight : 0 },
            ],
            skillsearch : ""
        }
    },
    methods:{
        updateList(){

        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.skillset{
    width: 80%;
    margin: auto;
    padding-bottom: 50px;
}

.skills{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.skill{
    width: 33%;
}

input{
    width: 50%;
    text-align: center;
    padding: 10px;
    font-size: 24px;
    border-radius: 13px;
}

.hidden{
    display: none;
}

@media screen and (max-width: 1080px) {
    input{
        width: 80%;
    }
}

@media screen and (max-width: 720px) {
    .skill{
        width: 80%;
    }
}
</style>
