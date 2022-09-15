<template>
    <div class="profexperience">
        <h1>Professional Experience</h1>
        <div class="experience" v-for="workplace in workplaces" :key="workplace.name">
            <h3>{{workplace.name}}</h3>
            <div>{{workplace.title}}</div>
            <div>{{workplace.startdate}} - {{workplace.enddate}}</div>
            <ul>
                <li v-for="responsibility in workplace.responsibilities" :key="responsibility.id">{{responsibility.description}}</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProfessionalExperience',
    data : function(){
        return{
            workplaces : [
                {
                    name : "Scam Takedown Task Force",
                    title : "Owner - Software Developer",
                    startdate : "April 2020",
                    enddate : "Current",
                    responsibilities : [ 
                        { id : 0, description : "Created a system from the ground up using Vue javascript framework that actively scans websites for key indicators of suspicious activity and automatically record findings for human review" },
                        { id : 1, description : "Designed and developed a system where results found by the computer can be reviewed by a human and voted on before being added to a growing database of over 60,000 sites" },
                        { id : 2, description : "Created plugins for both Chrome and Firefox that warn users when they enter a website that has been flagged as a scam in the database" },
                        { id : 3, description : "Developed a website that gives access to information about the project - along with configuring the website hosting and MYSQL database that hosts all of the data" },
                        { id : 4, description : "Created the backend points that create access points to the various data points using Node.js" },
                        { id : 5, description : "Activily monitor and troubleshoot all systems involved to ensure server health and acceptable user experiences" },
                        { id : 6, description : "Ongoing continuation of improving data collection of scam sites to further increase effeciency and user experiences" },
                    ]
                },
                {
                    name : "Clinton Grove Cemetery",
                    title : "Software Developer",
                    startdate : "March 2021",
                    enddate : "Current",
                    responsibilities : [ 
                        { id : 0, description : "Redesigned their website and reconfigured the site to run smoother and faster with minimal extras" },
                        { id : 1, description : "Recreated an Admin Interface using Vue.js framework that allowed the quick sorting and finding of information pertaining to the over 35,000 customer records in the database" },
                        { id : 2, description : "Recreated the backend system to use Node.js instead of PHP" },
                        { id : 3, description : "Updated their Geneolgy search abilities to correctly function while still using the PHP code it was written in based on the new backend system" },
                        { id : 4, description : "Developed a work order system in Vue.js that allows the grounds crew to provide near real time updates as jobs are completed" },
                        { id : 5, description : "Actively designing the system to track the space usage of the cemetery, with data to show where everyone is correctly position - complimented with GPS and pictures" },
                        { id : 6, description : "Activily monitoring and troubleshoot all systems involved to ensure server health and acceptable user experiences" },
                    ]
                },
                {
                    name : "Manufacture and Design Electronics",
                    title : "Software Engineer / IT",
                    startdate : "September 2014",
                    enddate : "May 2020",
                    responsibilities : [ 
                        { id : 0, description : "Developed an Inventory Management System and the procedures in order to train and seat employees within the position" },
                        { id : 1, description : "Created a replacement MRP (Material Resource Planning) system that is currently still in use within the facility using C#" },
                        { id : 2, description : "Developed a visioning system that leveraged NodeJS, C# and MYSQL to test if the products being produced operated correctly" },
                        { id : 3, description : "Worked on several projects that related to smaller needs of the company with Angular 6/7, such as reports and production scheduling" },
                        { id : 4, description : "Experience working with microcontrollers utilizing Node.JS" },
                    ]
                },
            ]
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.profexperience{
    margin-top: 50px;
}

.experience{
    width: 80%;
    margin: auto;
}

li{
    margin: 15px auto;
}
</style>
