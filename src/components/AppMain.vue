<script>
import Card from './Card.vue'

export default {
    name: "AppMain",
    components: {
        Card
    },
    data() {
        return {
            cards: [
                {
                    thumb: "https://static.dc.com/2023-03/LEGIONOB_Cv1_00111_DIGITAL.jpg?w=640",
                    price: "$19.99",
                    series: "DC'S LEGION OF BLOOM",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/FLS_Cv795_79511_DIGITAL.jpg?w=640",
                    price: "$3.99",
                    series: "THE FLASH",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/NTW_Cv102_10211_DIGITAL-1.jpg?w=640",
                    price: "$16.99",
                    series: "NIGHTWING",
                    type: "graphic novel"
                },
                {
                    thumb: "https://static.dc.com/2023-03/BMSMWF_Cv13_01311_DIGITAL.jpg?w=640",
                    price: "$2.99",
                    series: "BATMAN/SUPERMAN: WORLD'S FINEST",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/CTW_Cv53_05311_DIGITAL.jpg?w=640",
                    price: "$3.99",
                    series: "CATWOMAN",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/BA_Cv9_00911_DIGITAL.jpg?w=640",
                    price: "$2.99",
                    series: "BLACK ADAM",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/SM_LOST_Cv1_00111_DIGITAL.jpg?w=640",
                    price: "$3.99",
                    series: "SUPERMAN: LOST",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/SUPES_Cv2_00211_DIGITAL.jpg?w=640",
                    price: "$4.99",
                    series: "SUPERMAN",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/ROBIN_v3%20%28Cover%29.jpg?w=640",
                    price: "$5.99",
                    series: "ROBIN VOL. 3: SECRETS AND SHADOWS ",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/HQv3%20%28%20Cover%29.jpg?w=640",
                    price: "$6.99",
                    series: "HARLEY QUINN VOL. 3: VERDICT",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/MULTVTJ%20%28COVER%29.jpg?w=640",
                    price: "$4.99",
                    series: "MULTIVERSITY: TEEN JUSTICE",
                    type: "comic book"
                },
                {
                    thumb: "https://static.dc.com/2023-03/WW_Cv797_79711_DIGITAL.jpg?w=640",
                    price: "$16.99",
                    series: "WONDER WOMAN",
                    type: "graphic novel"
                }
            ]
        }
    }
}

</script>

<template>
    <main>
        <div class="container">

            <!-- bottone current -->
            <a href="#" class="button current">CURRENT SERIES</a>

            <!-- contenitore padre che contiene singola card -->
            <div class="cards">
                <Card v-for="card in cards" :thumb="card" />
            </div>

            <!-- bottone load -->
            <a href="#" class="button load">LOAD MORE</a>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as *;

main {
    background-color: #1c1c1c;

    .container {
        color: $text-white;
        text-align: center;
        padding: 30px 0;
        position: relative;

        .cards {
            display: flex;
            flex-wrap: wrap;
            margin-inline: -15px;
        }

        .button {
            display: inline-block;
            color: $text-white;
            background-color: $primary;
            font-weight: bolder;
            margin-top: 20px;

            &.current {
                padding: 10px 20px;
                position: absolute;
                left: 0;
                top: -40px;
            }

            &.load {
                padding: 10px 40px;
            }
        }
    }
}
</style>
