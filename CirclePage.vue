<template>
    <div class="container-fluid">
        <div class="row d-flex justify-content-center align-items-center p-0" style="height: 600px">
            <div class="natija col-12 text-center p-0 m-0 position-absolute">
                <span class="text">Natija</span>
            </div>
            <div
                class="col-6 col-md-4 col-lg-3 p-0 d-flex justify-content-center align-items-center flex-column position-relative"
                style="height: 300px">
                <div
                    class="col-12 col-md-8 col-lg-4 card d-flex justify-content-center align-items-center border-0 ms-1"
                    style="height: 200px">
                    <div class="circle" :class="calcPercentOfRightAnswers()">
                        <div class="value-container">{{ correctAnswers }}</div>
                    </div>
                </div>
                <span class="card-text">To'gri</span>
            </div>

            <div
                class="col-6 col-md-4 col-lg-3 d-flex justify-content-center align-items-center flex-column position-relative"
                style="height: 300px">
                <div
                    class="col-12 col-md-8 col-lg-4 card d-flex justify-content-center align-items-center border-0 ms-2"
                    style="height: 200px">
                    <div class="circle" :class="calcPercentOfWrongAnswers()">
                        <div class="value2-container">{{ incorrectAnswers }}</div>
                    </div>
                </div>
                <span class="card-text">Xato</span>
            </div>
            <div class="col-12 col-md-8 col-lg-6 btn-btn d-flex justify-content-around position-absolute">
                <a class="button-1" href="#">Qayta ishlash</a>
                <a class="button" href="#">Ortga qaytish</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "CirclePage",
    data() {
        return {
            testCount: 20,
            correctAnswers: 8,
            incorrectAnswers: 12,
        }
    },
    methods:
        {
            calcPercent(percent) {
                if (percent <= 10) {
                    return '10-percent';
                }

                if (percent <= 20) {
                    return '20-percent';
                }

                if (percent <= 30) {
                    return '30-percent';
                }

                if (percent <= 40) {
                    return '40-percent';
                }

                if (percent <= 50) {
                    return '50-percent';
                }

                if (percent <= 60) {
                    return '60-percent';
                }

                if (percent <= 70) {
                    return '70-percent';
                }

                if (percent <= 80) {
                    return '80-percent';
                }

                if (percent <= 90) {
                    return '90-percent';
                }

                if (percent <= 100) {
                    return '100-percent';
                }
            },

            calcPercentOfRightAnswers() {
                let percent = this.correctAnswers * 100 / this.testCount
                return'circle-' + this.calcPercent(percent)
            },

            calcPercentOfWrongAnswers() {
                let percent = this.incorrectAnswers * 100 / this.testCount
                return 'circle2-' + this.calcPercent(percent)
            }
        },
}
</script>

<style scoped lang="css">
.circle {
    height: 150px;
    width: 150px;
    border-radius: 50%;
    display: grid;
    place-items: center;
}

.circle:before {
    content: '';
    position: absolute;
    height: 130px;
    width: 130px;
    border-radius: 50%;
    background-color: white;
}

.card-text {
    font-family: 'Averta Demo', sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    color: #1A3447;
}

.circle-10-percent {
    background: conic-gradient(#0467FF 36deg, white 0deg);
}

.circle-20-percent {
    background: conic-gradient(#0467FF 72deg, white 0deg);
}

.circle-30-percent {
    background: conic-gradient(#0467FF 108deg, white 0deg);
}

.circle-40-percent {
    background: conic-gradient(#0467FF 144deg, white 0deg);
}

.circle-50-percent {
    background: conic-gradient(#0467FF 180deg, white 0deg);
}

.circle-60-percent {
    background: conic-gradient(#0467FF 216deg, white 0deg);
}

.circle-70-percent {
    background: conic-gradient(#0467FF 252deg, white 0deg);
}

.circle-80-percent {
    background: conic-gradient(#0467FF 288deg, white 0deg);
}

.circle-90-percent {
    background: conic-gradient(#0467FF 324deg, white 0deg);
}

.circle-100-percent {
    background: conic-gradient(#0467FF 360deg, white 0deg);
}

.value-container {
    font-family: Averta Demo, sans-serif;
    position: relative;
    color: blue;
    font-size: 60px;
}

.circle2-10-percent {
    background: conic-gradient(#FA404B 36deg, white 0deg);
}

.circle2-20-percent {
    background: conic-gradient(#FA404B 72deg, white 0deg);
}

.circle2-30-percent {
    background: conic-gradient(#FA404B 108deg, white 0deg);

}

.circle2-40-percent {
    background: conic-gradient(#FA404B 144deg, white 0deg);

}

.circle2-50-percent {
    background: conic-gradient(#FA404B 180deg, white 0deg);

}

.circle2-60-percent {
    background: conic-gradient(#FA404B 216deg, white 0deg);

}

.circle2-70-percent {
    background: conic-gradient(#FA404B 252deg, white 0deg);
}

.circle2-80-percent {
    background: conic-gradient(#FA404B 288deg, white 0deg);
}

.circle2-90-percent {
    background: conic-gradient(#FA404B 324deg, white 0deg);
}

.circle2-100-percent {
    background: conic-gradient(#FA404B 360deg, white 0deg);
}

.value2-container {
    font-family: Averta Demo, sans-serif;
    position: relative;
    color: #FA404B;
    font-size: 60px;
}

.text {
    font-family: 'Averta Demo', sans-serif;
    font-weight: 400;
    font-size: 30px;
    color: #000000;
    text-align: center;
}

.natija {
    top: 13em;
}

.btn-btn {
    bottom: 7em;
}

.button-1 {
    width: 115px;
    height: 30px;
    border: 1px solid #01FF88;
    border-radius: 4px;
    color: #000000;
    text-decoration: none;
    text-align: center;
    padding: 2px;
}

.button {
    width: 115px;
    height: 30px;
    border: 1px solid #0467FF;
    border-radius: 4px;
    color: #000000;
    text-decoration: none;
    text-align: center;
    padding: 2px;
}

</style>