<script>
    import LightSlider from "./lib/LightSlider.svelte";
    import Light from "./lib/Light.svelte";

    let data = {
      lightOne: false,
      lightTwo: false
    }

    let collectors = [];

    function register(fn){
      collectors.push(fn);
    }

    function sendData(){ 
      const allData = collectors.map(fn => fn());
      console.log(allData);
    }
</script>

<div class = "app">
  <h1>Light Controller</h1>

  <button onclick={sendData}>Send To Light</button>
  
  <!-- First Light Controller-->
  <Light title = "One" register={register}/>

  <!-- Second Light Controller -->
  <Light title = "Two" register={register}/>
</div>

<style>
  button {
    background-color: #B7245C;

    border-color: #7C3238;
    border-radius: 1vh;
    color: #002500;

    width: 15vh;
    height: 7vw;
  }
</style>
