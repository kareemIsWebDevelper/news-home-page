<script>
    export default {
        data: function (){
            return {

            }
        }
    }
</script>

<template>
    <div id="grid-items">
        <div id="content">
            <div class="web-image"></div>
            <div class="flex-box">
                <h1 class="m">The Bright<br> Future of Web<br> 3.0?</h1>
                <h1 class="d">The Bright<br> Future of<br> Web 3.0?</h1>
                <div class="grid-box">
                    <p>We dive into the next evolution of the web that<br> claims to put the power of the platforms back<br> into the hands of the people.But is it really<br> fulfilling its promise?</p> 
                    <button >READ MORE</button>
                </div>
            </div>
        </div>
    
        <div id="new-column">
            <div class="new">
                <h1>New</h1>
                <h3>Hydrogen VS Electric Cars</h3>
                <p>Will hydrogen-fueled cars ever catch up<br> to EVs?</p>
                <hr>
                <h3>The Downsides of AI Artistry</h3>
                <p>What are the possible adverse effects of<br> on-demand AI image generation?</p>
                <hr>
                <h3>Is VC Funding Drying Up?</h3>
                <p>Private funding by VC firms is down 50%<br> YOY. We take a look at what that means.</p>
            </div>
        </div>
    </div>

    <div id="row">
        <div class="column">
            <img src="../assets/images/image-retro-pcs.jpg">
            <div class="info">
                <h1>01</h1>
                <p class="black-para">Reviving Retro PCs</p>
                <p>What happens when old PCs<br> are given modern upgrades?</p>
            </div>
        </div>

        <div class="column">
            <img src="../assets/images/image-top-laptops.jpg">
            <div class="info">
                <h1>03</h1>
                <p class="black-para">Top 10 Laptops of 2022</p>
                <p>Our best picks for various<br>needs and budgets.</p>
            </div>
        </div>

        <div class="column">
            <img src="../assets/images/image-gaming-growth.jpg">
            <div class="info">
                <h1>02</h1>
                <p class="black-para">The Growth of Gaming</p>
                <p>How the pandemic has sparked<br>fresh opportunities.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
#content,.grid-box
,#new-column,.new{
    flex-wrap: wrap;
}
    .web-image {
        background: url(../assets/images/image-web-3-mobile.jpg);
        background-size: 100% 100%; 
        width: 350px;
        height: 300px;
    }

    .m {
        font-size: 42px;
        line-height: 40px;
    }

    .d {
        display: none;
    }

    p {
        color: hsl(236, 13%, 42%);
        font-size: 15px;
    }

    button {
        color: hsl(36, 100%, 99%);
        background-color: hsl(5, 85%, 63%);
        width: 200px;
        height: 42px;
        letter-spacing: 3px;
        border: none;
        margin-top: 15px;
    }

    button:hover {
        background-color: black;
        cursor: pointer;
    }

    #new-column {
        background-color: hsl(240, 100%, 5%);
        width: 350px;
        height: auto;
        margin: 30px auto auto auto;
    
    }

    .new {
        padding: 20px;
        width: 310px;
        margin: auto;
    }
    .new p {
        color: hsl(236, 13%, 42%);
    }
    .new h1 {
        color: hsl(35, 77%, 62%);
    }
    .new h3 {
        color: hsl(36, 100%, 99%);
        margin-top: 30px;
        margin-bottom: 30px;
    }
    .new h3:hover {
        color: hsl(35, 77%, 62%);
        cursor: pointer;
    }

    hr {
        background-color: hsl(236, 13%, 42%);
    }

    #row {
        display: flex;
        flex-flow: column;
        justify-content: flex-start;
        height: 130px;
        gap: 30px;
        margin-top: 30px;
        height: 550px;
    }

    .column {
        display: flex;
        height: 130px;

    }
    .column img {
        width: 100px;
        height: 130px;
    }

    .info {
        height: inherit;
        text-align: left;
        margin-left: 20px;
    }
    .info h1 {
        color: hsl(233, 8%, 79%);
    }

    .black-para {
        color: black;
        font-weight: 900;
        font-size: 17px;
        margin-top: -20px;
        margin-bottom: -5px;
    }
    .black-para:hover {
        color: hsl(5, 85%, 63%);
        cursor: pointer;
    }

    @media screen and (min-width: 400px) {
        #grid-items {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            gap: 30px;
        }
        #content {
            width: 65%;
            height: 450px;
        }
        .web-image {
            background: url(../assets/images/image-web-3-desktop.jpg);
            background-size: 100% 100%; 
            width: auto;    /* the same width of parent(#content)*/
            height: 280px;
        }
        .m {
            display: none;
        }
        .d {
            display: block;
            font-size: 40px;
            font-weight: 800;
            line-height: 40px;
        }

        .flex-box {
            display: flex;
            justify-content: space-between;
        }

        .grid-box {
            margin-right: 20px;
        }

        #new-column {
            background-color: hsl(240, 100%, 5%);
            font-size: 15px;
            margin-top: 0;
            width: 300px;
            height: 435px;
        }

        .new {
            margin-top: -20px;
            width: 260px;
        }

        .new br {
            display: none;
        }
        .new h3 {
            margin-top: 30px;
            margin-bottom: 0;
        }

        hr {
            width: 250px;
            margin: auto;
        }

        #row {
            display: flex;
            flex-flow: row;
            height: 130px;
            gap: 60px;
        }
        
        .black-para {
            font-size: 13px;
        }
    }
</style>