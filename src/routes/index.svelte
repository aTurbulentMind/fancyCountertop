<body>
    

        <div class="art-banner" id="art-banner">
        <div class="art-banner-bg"></div>
        <div class="banner-text">Artistic <br>Artisian <br> Countertops</div>

        <div class="form">
        <container>
        <form action="https://formsubmit.co/joelkrivers@gmail.com" method="POST">
            <wrapper>
                <box>
                    <input type="text" name="email" id="email" placeholder="Phone or Email" required>
                    <input type="hidden" name="_next" value="https://www.lanternlightdevelopment.com/contact">
                    
                </box>
            </wrapper>
            <br>
            <button type="submit">Contact</button>
        </form>
    </container>
    </div>

        <a href="/" class="soc"><svg viewBox="0 0 178 136" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M91.8925 113.333V78.1999H80.3225V64.3733H89.89C90.3328 64.3733 91.1827 64.4254 91.5365 64.1421C91.9148 63.8361 91.8836 63.2286 91.8925 62.7866V58.7066C91.8925 52.3237 91.828 46.5527 96.3803 41.4822C100.639 36.7426 106.048 36.2575 111.917 36.2666L115.255 36.4933L119.705 36.7199V49.1866L111.027 49.3521C109.432 49.5855 108.171 49.8439 107.116 51.2311C106.355 52.2285 106.148 53.6225 106.132 54.8533V62.3333C106.137 64.0854 106.104 64.3597 107.912 64.3733H119.26L117.702 78.1999H106.132V113.333H128.382C131.822 113.329 133.496 111.624 133.5 108.12V93.6133V27.8799C133.496 24.455 131.751 22.6711 128.382 22.6666H114.142H49.6175C46.2934 22.6711 44.5045 24.5026 44.5 27.8799V42.3866V108.12C44.5 108.804 44.4778 109.498 44.678 110.16C45.083 111.493 46.3067 112.739 47.615 113.152C48.6541 113.478 54.1454 113.333 55.625 113.333H91.8925Z" fill="#3B5998"  />
</svg>
 </a>
       </div>
       <h1>Words</h1>

       <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi tempora sint rem voluptatum reprehenderit repellendus facere ad a totam assumenda! Dolorum maxime mollitia fugit ipsum odit praesentium autem, quo distinctio commodi iusto! Corporis praesentium laudantium saepe enim commodi vero voluptate!</p>

       <h2>Other words.</h2>

       <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Laudantium placeat aut maiores ea facilis corrupti quibusdam suscipit enim facere beatae?</p>

       <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae, nesciunt doloremque accusamus odit similique, minus impedit qui tempore tempora veritatis, eligendi optio sequi provident.</p>


       <places>
           <location>
                <div class="card">
                  <div class="content">
                    <h2>Mr Amazo</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim asperiores numquam veritatis dolores nihil nostrum eius facilis?</p>
                    <a href="/">Blah bla blah</a>
                  </div>    
                   <img src="/img/silenceIsGoldenXXX.png" alt="">
                </div>
           </location>

           <location>
                <div class="card">
                  <div class="content">
                    <h2>Mr Amazo</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim asperiores numquam veritatis dolores nihil nostrum eius facilis?</p>
                    <a href="/">Blah bla blah</a>
                  </div>    
                   <img src="/img/silenceIsGoldenXXX.png" alt="">
                </div>
           </location>

           <location>
                <div class="card">
                  <div class="content">
                    <h2>Mr Amazo</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim asperiores numquam veritatis dolores nihil nostrum eius facilis?</p>
                    <a href="/">Blah bla blah</a>
                  </div>    
                   <img src="/img/silenceIsGoldenXXX.png" alt="">
                </div>
           </location>

           <location>
                <div class="card">
                  <div class="content">
                    <h2>Mr Amazo</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim asperiores numquam veritatis dolores nihil nostrum eius facilis?</p>
                    <a href="/">Blah bla blah</a>
                  </div>    
                   <img src="/img/silenceIsGoldenXXX.png" alt="">
                </div>
           </location>

           <location>
                <div class="card">
                  <div class="content">
                    <h2>Mr Amazo</h2>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim asperiores numquam veritatis dolores nihil nostrum eius facilis?</p>
                    <a href="/">Blah bla blah</a>
                  </div>    
                   <img src="/img/silenceIsGoldenXXX.png" alt="">
                </div>
           </location>
       </places>
</body>
           

 

<style lang="scss">
    @import 'components';

    
.art-banner {
    height: 100vh;
    display: grid;
    background:$gradient;
    grid-template-columns: 20px 1fr 1fr 1fr 20px;
    grid-template-rows: 20px 1fr 1fr 1fr 20px;
    margin: 5px 0;
    z-index: 99;

    svg{
        width: 50%;
    }

    input,
    textarea{
        width: 100%;
        font-size: 3vw;
        background: $backgroundThird;
        border: none;
        border-radius:2px;
        outline: none;
        border-bottom: 1px solid $textColorMain;
        transition:0.3s linear;
    }

    input:focus,
    input:valid,
    textarea:focus,
    textarea:valid{
        padding: 10px;
        color: $textColorMain;
        background: $backgroundSecond;
        margin: 10px;
        border-radius:4px;
        font-size: 2.5vw;
    }

    .soc {
        grid-column: 4;
        grid-row: 4;
        z-index: 10;
    }
}

.art-banner-bg {
    
    background-size: 100%;
    opacity: 0.25;
    grid-column: 1 / -1;
    grid-row: 1 / -1;

    img {
        width: 100%;
        padding: 15%;
    }
}

.banner-text {
    font-size: 11.5vw;
    font-weight: bold;
    grid-column: 2 / span 2;
    grid-row: 2 /* no need to type one*/;
    align-self: center;
    justify-self: center;
    z-index: 3;
}

.form {
    grid-column: 2;
    grid-row: 4;
    z-index: 10;
}

button{
    background: rgba(16, 15, 17, 0.616);
        outline: none;
        font-weight: 100;
        letter-spacing: 4px;
        border: 1px solid $extra;
        border-radius:4px;
        color: $textColorMain;
        text-transform: uppercase;
        padding: 5px;
        margin: 4%;
        font-family: $mainFont;

        &:hover {
           transition: all 0.3s ease-in-out;
        background: $textColorMain;
        color: $backgroundMain;
        font-weight: 800;
        transform: scale(1.05);
        cursor: pointer;
        }
}

    places{
        
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        gap: 4%;
        margin: 2% 4% 17% 4%;


        svg{
            width: 70%;
            margin:0 25%;
        }

    }

    .card{
        position: relative;
        width: 600px;
        height: 350px;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        border-radius: 20px;
    }

    .card:hover{
        @include glassBack();
        transition: 0.45s ease-in-out;
        width: 75%;
        margin: 3%;
    }

    .card img{
        position: absolute;
        bottom: 0;
        left: 50%;
        transform: translateX(-50%);
        height: 400px;
        transition: 0.5s;
    }

    .card:hover img{
        left: 80%;
        height: 400px;
        transform: rotateY('90deg');
    }

    .card .content{
        position: relative;
        left: 20%;
        width: 50%;
        padding: 20px 20px 20px 40px;
        opacity: 0;
        visibility: hidden;
        transition: 0.3s;
        text-transform: uppercase;
    }

    .card:hover .content{
        left: 0%;
        opacity: 1;
        visibility: visible;
    }

    .card .content h2{
        font-size: 2.25vw;
        font-weight: bold;
        margin:0 0 10px 0;
        text-transform: uppercase;
    }

    .card .content p{
        font-size: 1.8vw;
        margin: 8% 5%;
    }

    .card .content a{
        position: relative;
        display: inline-block;
        font-size: 1.8vw;
        text-decoration: none;
        transition: 0.3s;
        padding: 10px 20px;
        border-radius: 20px;
        margin-top: 10px;
        background: rgba(16, 15, 17, 0.616);
        outline: nonrgba(15, 17, 15, 0.616)  ;
        font-weight: 100;
        letter-spacing: 2px;
        border: 1px solid $extra;
        color: $textColorMain;
        text-transform: uppercase;


        &:hover {
        transition: all 0.3s ease-in-out;
        background: $textColorMain;
        color: $backgroundMain;
        font-weight: 800;
        transform: scale(1.1);
        cursor: pointer;
        font-size: 2.4vw;
        box-shadow: 0 0 15px 8px $Glow;
        }
    }


</style>