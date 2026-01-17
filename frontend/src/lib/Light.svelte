<script>
    import LightSlider from "./LightSlider.svelte";


    let {title, onSave} = $props();
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
            Cycle between multiple colors
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
        margin-bottom: 1vw;
        margin-top: 1vw;
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
        gap: 0.1rem;
        margin-bottom: 0.1vh;
    }

    .generalSettings input[type="number"]{
        width: 10ch;
    }

    h2{
        margin-top: 0.5vh;
        margin-bottom: 0vh;
    }
    h3{
        margin-bottom: 0vh;
        padding: 0vh;
    }

    p{
        margin-top: 0;
        margin-bottom: 0vh;
    }

    label{
        margin-top:1vh;
    }
</style>