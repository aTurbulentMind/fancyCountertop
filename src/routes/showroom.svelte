<body>
    

	<h1>Showroom</h1>


    <places>
        <room>
            <a href="/bathroom/">
            <h2>Bathroom</h2>
            <img src="/img/hitkin.jpg/" alt="">
            </a>
        </room>

        <room>
            <a href="/">
            <h2>Kitchen</h2>
            <img src="/img/hitkin.jpg/" alt="">
            </a>
        </room>

        <room>
            <a href="/">
            <h2>Islands</h2>
            <img src="/img/hitkin.jpg/" alt="">
            </a>
        </room>

        <room>
            <a href="/">
            <h2>Outdoor features</h2>
            <img src="/img/hitkin.jpg/" alt="">
            </a>
        </room>
    </places>
</body>
	

<style lang="scss">
	@import 'components';

	places{
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr;
        gap: 8%;
        margin: 2% 4% 20% 4%;

        a{
            color: $textColorMain;
        }

        h2{
            margin: 4%;
        }

        @media (max-width: 768px) {
            grid-template-columns: 1fr;
            grid-template-rows: 1fr 1fr 1fr 1fr;
            margin-bottom: 100%;
        }

    room{
        border-radius: 10px;
        background: #12770525;
        box-shadow: 0 3px 12px 3px $backgroundThird;
        border: 1px solid #0c721463;

        &:hover{
                transition: 0.3s;
                transform: scale(1.05);
            }

        img{
            box-shadow: 0 3px 12px 3px $backgroundThird;
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 0 0 10px 10px;
        }
    }

        

    }

</style>
