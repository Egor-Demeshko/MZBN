<script>
    let blurEffect = 20;
</script>

<video class="background" src="/bubbles.mp4" loop autoplay muted playsinline>
</video>
<div class="blur" style="backdrop-filter: blur({blurEffect}px);">

</div>

<div class="header">
    <p>СТЕКЛО</p>
    <p>НЕСТЕКЛО</p>
</div>

<div class="fishka">
    <h1>Супер важная фишка</h1>
</div>

<div class="fishka2">
    <h1>ТУТ нет стекла</h1>
</div>

<div class="range">
    <input  type="range" bind:value={blurEffect}/>
</div>

<style>
    :global(body){
        margin: 0;
    }
    * *{
        box-sizing: border-box;
    }

    .background {
        width: 100vw;
        height: 100vh;
        box-sizing: border-box;
        object-fit: cover;
    }

    .blur{
        background-color: #24018323;
        width: 50vw;
        height: 100vh;
        position: fixed;
        top: 0;
        left: 0;
    }

    .header{
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100px;
        display: flex;
        justify-content: space-around;
        align-items: center;
        backdrop-filter: blur(30px);
        box-shadow: 0 0 6px black;
    }

    p{
        color: white;
        font-size: 24px;
        font-weight: bold;

    }


    h1{
        font-size: 48px;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    }

    .fishka{
        height: 250px;
        width: 482px;
        background-color: #75747466;
        position: absolute;
        left: 50%;
        top: 20%;
        transform: translate(-50%);
        border: 10px solid transparent;
        border-radius: 20px;
        background-color: #d3d3d366;
        /*
        border-image: linear-gradient(to right, #f00, #0f0) round;
        border-image-slice: 1;
        */
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: beige;
        backdrop-filter: blur(10px);
        --webkit-backdrop-filter: blur(10px);
    }


    .fishka::before{
        content: "";
        position: absolute;
        height: 266px;
        width: 494px;
        border-radius: 20px;
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
        mask: linear-gradient(#fff 0 0) padding-box, 
     linear-gradient(#fff 0 0);
        -webkit-mask-composite: xor;
        mask-composite: exclude;
        background: linear-gradient(to left, rgba(151, 23, 0, 0.7), rgba(255, 255, 255, 0.164)) border-box;
        border: 4px solid transparent;
    }


    .fishka2{
        height: 250px;
        width: 484px;
        background-color: #323232BF;
        position: absolute;
        left: 50%;
        top: 60%;
        transform: translate(-50%);
        border-radius: 20px;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
        color: beige;
    }

    .range{
        position: absolute;
        left: 10%;
        top: 70%;
        display: block;
        z-index: 10;
    }
</style>