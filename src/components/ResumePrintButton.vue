<template>
    <div>
        <div class="info">//This button is for those who prefer to have a piece of paper to read</div>
        <a href="/danielstokesresume.pdf" target="_blank">
            <div class="printbutton" :class="{ hackermode : hackermode }">
                Console.log(resume)
            </div>
        </a>
    </div>
</template>

<script>
export default {
    name: 'ResumePrintButton',
    props: {
        hackermode : Boolean
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