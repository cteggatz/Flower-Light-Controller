<script>
    import LightSlider from "./lib/LightSlider.svelte";
    import Light from "./lib/Light.svelte";

    function handleOneData(data){

    }

    function handleTwoData(data){

    }

</script>

<div class = "app">
  <h1>Light Controller</h1>

  <button>Send To Light</button>
  
  <!-- First Light Controller-->
  <Light title = "One" onSave="handleOneData"/>

  <!-- Second Light Controller -->
  <Light title = "Two" onSave="handleTwoData"/>
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
