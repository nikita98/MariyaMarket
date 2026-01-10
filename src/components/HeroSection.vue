<template>
    <div class="hero">
        <img class="hero__bg" alt="" src="../assets/horseBG.png">
        <div class="hero__bg_shadow"></div>
        <div class="container">
            <div class="row">
                <div class="hero__text">
                    <!-- <div class="logo">
                        <img class="logo__img" alt="Vue logo" src="../assets/logo.png">
                    </div> -->
                    <h1 class="fw-bold">


                        <div class="white">Ярмарка выходного дня</div>
                        <br>
                        «Маруся Маркет»

                    </h1>
                    <h2>Товары ручной работы, вкусная еда <br> мастер-классы для детей и взрослых</h2>
                    <div class="hero__info-items">
                        <div class="hero__info-items-container">
                            <!-- <div class="hero__info-item">
                                <div class="hero__info-icon">📅</div>
                                <span>17, 24, 31 января 2026</span>
                            </div>
                            <div class="hero__info-item">
                                <div class="hero__info-icon">🕚</div>
                                <span>Начало в 11:00</span>
                            </div>
                            <div class="hero__info-item">
                                <div class="hero__info-icon">📍</div>
                                <span>ТЦ Пальмира 2 этаж</span>
                            </div> -->
                            <a href="#contacts" class="btn button hero__btn col-3">
                                Посетить бесплатно
                            </a>
                        </div>

                    </div>

                    <!-- <a href="#info" class="btn btn-danger btn-lg mt-3">
                        Посетить бесплатно
                    </a> -->
                </div>
            </div>

        </div>
    </div>
</template>


<style scoped>
.hero {
    width: 100%;
    height: 100vh;
    overflow: hidden;
    position: relative;
    display: flex;
    justify-content: start;
    align-items: flex-end;

    .hero__bg {
        width: 100%;
        position: absolute;
        left: 0;
        top: 50%;
        transform: translateY(-50%);
        min-height: 100%;
    }

    .hero__bg_shadow {
        height: 100%;
        width: 100%;
        position: absolute;
        left: 0;
        top: 0;
        background-color: rgba(0, 0, 0, 0.4);
        display: block;
    }

    .hero__container {
        height: 100%;
        z-index: 2;
        position: relative;
        display: flex;
        align-items: flex-end;
        height: 100%;
        padding-bottom: 20%;
        padding-top: 80px;
    }

    .hero__text {
        z-index: 1;
        text-align: left;
        color: white;

        h1 {
            color: var(--primary-red);
        }

        .white {
            display: inline;
            color: white;
        }

        p {
            color: white;
        }
    }

    .hero__info-items {
        display: flex;
        flex-direction: column;
        align-items: start;
        margin-top: 30px;
    }

    .hero__info-item {
        color: #000;
        display: flex;
        align-items: center;
        gap: 15px;
        font-size: 1.1rem;
        padding: 10px 20px;
        margin-bottom: 10px;
        height: 60px;
        background: var(--bg-warm);
        border-radius: 12px;
        box-shadow: var(--shadow-soft);
    }

    .hero__info-icon {
        width: 45px;
        height: 45px;
        background: var(--primary-red);
        border-radius: 50%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.3rem;
    }

    .hero__btn {
        margin-top: 20px;
        width: 300px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: 500;
    }

}

.logo {
    overflow: hidden;
    position: relative;
    border-radius: 100%;
    padding-top: 100%;
    width: 100px;

    .logo__img {
        position: absolute;
        height: 100%;
        width: 100%;
        left: 0;
        top: 0;
    }
}
</style>