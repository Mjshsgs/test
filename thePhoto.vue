<script>
    export default {

        name: 'ThePhoto',
        data() {
            return {
                likes: 0,
                dislikes: 0,
            }
        },
        methods: {
            getImage() {
                axios.get("https://api.api-ninjas.com/v1/randomimage?category=family", {
                    headers: {
                        "X Api-Key": "87P830Ugro3fiyRg8GfTdQ==YeEFB9AGOabmVsMx",
                        "Accept": "image/jpg"
                    }
                }).then((res) => {
                    console.log('res', res);
                }).batch((err) => {
                    console.error(err.message);
                })
            },

            addLike: function () {

                this.likes++

            },

            adddislike: function () {

                this.dislikes++

            }
        }

    }
</script>
<template>
    <div class="container">
        <ul class="h1">Kiberstam</ul>
        <div class="card">
            <div class="card__stats">
                <div class="card__likes"> {{ likes }} <img
                        src="https://cdn-icons-png.flaticon.com/512/10307/10307888.png"></div></div></div>
                <div class="card__dislikes"> {{ dislikes }} <img
                        src="https://cdn-icons-png.flaticon.com/512/3670/3670156.png"></div>
            </div>
            <div class="card__image"><img
                    src="https://media.istockphoto.com/id/937042470/ru/%D1%84%D0%BE%D1%82%D0%BE/%D1%81%D1%82%D0%B0%D0%B4%D0%B8%D0%BE%D0%BD.jpg?s=612x612&w=0&k=20&c=AJGWTh0eUB-PhEeHJLg_3JpRzm1RpzAT_-SrNzDnk38="
                    alt="Kiberone"></div>
            <div class="btns">
                <button class="btns__item btnL" @click="likes++">Like</button>
                <button class="btns__item btnD" @click="dislikes++">dislike</button>
            </div>

</template>
<style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat&family=Rubik:wght@500&display=swap');



    .container {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .card__image {
        position: absolute;
        width: 300px;
        margin-left: 500px;
    }

    .card__image img {
        width: 300px;
        object-fit: contain;
        margin-left: -150px;
        border-style: outset;
    }


    .btnD {
        font-size: 10px;
        position: absolute;
        margin-left: -100px;
        margin-top: 510px;
        background: linear-gradient(45deg, #590000, #ff2525);
        border-radius: 5px;
    }


    .btnL {
        font-size: 1px;
        position: absolute;
        margin-left: 15px;
        margin-top: 50px;
        background: linear-gradient(45deg, #254e02, #17ff0b);
        border-radius: 5px;
        margin-top: 51px;
        margin-left: 50px;
    }

    .h1 {
        position: absolute;
        width: 186px;
        height: 29px;
        left: 450px;
        top: 10px;

        font-family: 'Montserrat', sans-serif;   
        font-style: normal;
        font-weight: 400;
        font-size: 24px;
        line-height: 29px;

        color: #000000;
    }

    .hm {
        background: linear-gradient(45deg, #f0da17, #ff9100);
        width: 1060px;
        height: 70px;

    }

    .btnone {
        position: absolute;
        margin-left: 860px;
        margin-top: 10px;
        font-family: 'Montserrat', sans-serif;
    }

    .btntwo {
        position: absolute;
        margin-left: 950px;
        margin-top: 10px;
        font-family: 'Montserrat', sans-serif;
    }

    .btnthr {
        position: absolute;
        margin-left: 700px;
        margin-top: 10px;
        font-family: 'Montserrat', sans-serif;   
    }

    .btnfor {
        position: absolute;
        margin-left: 665px;
        margin-top: 10px;
        font-family: 'Montserrat', sans-serif;
        
    }


    .dislikes {
        width: 15px;
        height: 15px;
        margin-top: 50px;
    }

    .card_stats {
        display: flex;
    }

    .card__likes img {
        width: 15px;
        height: 15px;
        margin-top: 33px;
        
    }

    .card__dislikes img {
        width: 15px;
        height: 15px;
    }
    
    .card__dislikes {
        margin-top: 55px;
        
    }

    .card__likes {
        height: 50px;
        width: 100px;
        background: #000000(385, 255, 255, 0.5);
        margin-left: -160px;
        margin-top: 20px;
        
    }
</style>
