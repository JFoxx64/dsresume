<template>
    <div>
        <div class="info">//This button is for those who prefer to have a piece of paper to read</div>
        <a href="/files/dsresume.pdf" target="_blank" @click="logResume">
            <div class="printbutton" :class="{ hackermode : hackermode }">
                console.log(resume)
            </div>
        </a>
    </div>
</template>

<script>
export default {
    name: 'ResumePrintButton',
    props: {
        hackermode : Boolean
    },
    methods:{
        logResume(){
            console.log("The resume should have opened on a new tab!  It looks a lot better than it would in the console in the PDF or on the website.  You should be able to find it here: https://dstokes.us/files/dsresume.pdf")
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.printbutton{
    border: 1px solid rgb(135, 135, 135);
    width : 30%;
    padding: 10px;
    font-size: 24px;
    border-radius: 13px;
    margin: 10px auto;
    cursor: pointer;
    transition: 0.3s ease-in-out;
}

.printbutton:hover{
    background-color: #ccc;
}

.hackermode.printbutton:hover{
    background-color: #333;
}

a, a:hover, a:focus, a:active{
    color: unset;
    text-decoration: none;
}

.info{
    width: 80%;
    margin: auto;
}

@media screen and (max-width: 720px) {
    .printbutton{
        width: 80%;
    }
}
</style>