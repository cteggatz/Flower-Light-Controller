<script>
    import LightSlider from "./LightSlider.svelte";

    let {title} = $props();
    let cycleColors = $state(false);
</script>



<div id = "body">
    <h2>Light {title}</h2>

    <div class = "generalSettings">
        <h3>General Settings</h3>
        <p>These are general settings inside of the light</p>

        <label>
            Cycle Color:
            [<input type="checkbox" bind:checked={cycleColors}/>]
            <p>Cycle between multiple colors</p>
        </label> 
        {#if cycleColors}
            <label>
                Delay (Seconds):
                <input type="number" defaultValue="1" min = "0" width="5ch">
                How long in seconds between each light
            </label>
        {/if}
    </div>


    <h3>Light Settings</h3>
    <LightSlider title = "One"/>
    {#if cycleColors}
        <LightSlider title = "Two"/>
    {/if}
</div>

<style>
    #body {
        background-color: white;
        padding: 2vw;

        border-color: #929982;
        border-style: solid;
        border-radius: 1vh;
        border-width: 0.5vw;
    }

    .generalSettings {
        display: flex;
        flex-direction: column;
        gap: 0.1rem;
    }
  
    .generalSettings label {
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    .generalSettings input[type="number"]{
        width: 10ch;
    }

    

    h2{
        margin-top: 0.5vh;
    }
    h3{
        margin-bottom: 0.125vh;
    }
</style>