<script>
    let {title} = $props();

</script>

<div class = "light">
    <h3>Color {title}</h3>
    <div class = "inputs">
        <div class = "inputElements">
            <label for="colorInput">Color Seclection:</label>
            <input type="color" id = "colorInput"/>     
        </div>
        <div class = "inputElements">
            <label for = "intensity">Light Intensity [0 to 100]: </label>
            <input type="number"/>
        </div>
    </div>
</div>



<style>
    

    .light{
        background-color: #f5f5f5;
        border: 1px solid #929982;
        box-shadow: 0 1px 3px rgba(0, 37, 0, 0.1);
        border-radius: 1vh;

        padding: 0.5vw;
        margin-bottom: .5vh;
    }

    h3{
        margin-bottom: 0.125vh;
        margin-top: 1.5vh;
        margin-left: 1vh;
    }
    .inputs{
        display: flex;
        flex-direction: column;
    }

    .inputElements{
        margin: 0.5vh;
        padding:0.5vh;
        border-radius: 1vh;
    }
</style>