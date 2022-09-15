<template>
    <div id="app" :class="{ hackermode : hackermode }">
        <h1>Daniel Stokes</h1>
        <h3>Full time technology and software enthusiast, part time Scam Hunter</h3>
        <ul>
            <li>Michigan (Remote or Willing to Relocate)</li>
            <li>586.339.0569</li>
            <li>dan@scamtdtf.com</li>
        </ul>
        <h2>{{hackermode ? "Hacker View" : "Professional View"}}</h2>
        <label class="switch">
            <input type="checkbox" @change="hackermode = !hackermode">
            <span class="slider round"></span>
        </label>
        <ProfessionalView v-if="!hackermode"/>
        <HackerView v-if="hackermode"/>
    </div>
</template>

<script>
import ProfessionalView from './views/ProfessionalView.vue'
import HackerView from './views/HackerView.vue'

export default {
  name: 'App',
  components: {
    ProfessionalView,
    HackerView
  },
  data : function(){
    return{
      hackermode : false
    }
  },
  methods:{

  }
}
</script>

<style>
#app {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  min-height: 100%;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #414141;
  transition: 0.3s ease-in-out;
}

#app.hackermode{
  background-color: #414141;
  color: #ccc;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin: 5px auto;
}

 /* The switch - the box around the slider */
.switch {
  position: relative;
  display: inline-block;
  width: 60px;
  height: 34px;
  margin-bottom: 50px;
}

/* Hide default HTML checkbox */
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}

/* The slider */
.slider {
  position: absolute;
  cursor: pointer;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #ccc;
  -webkit-transition: .4s;
  transition: .4s;
}

.slider:before {
  position: absolute;
  content: "";
  height: 26px;
  width: 26px;
  left: 4px;
  bottom: 4px;
  background-color: white;
  -webkit-transition: .4s;
  transition: .4s;
}

input:checked + .slider {
  background-color: #444d55;
}

input:focus + .slider {
  box-shadow: 0 0 1px #b6b6b6;
}

input:checked + .slider:before {
  -webkit-transform: translateX(26px);
  -ms-transform: translateX(26px);
  transform: translateX(26px);
}

/* Rounded sliders */
.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}
</style>
