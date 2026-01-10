<template>
    <section class="container py-5 about">
        <h2 class="text-center mb-4 about__title">Что можно найти на ярмарке</h2>
        <div class="row g-4">
            <div class="col-md-6 col-lg-3">
                <div class="about__card border">
                    <div class="about__img-wrap">
                        <img src="../assets/album/horseLove.jpg" alt="" class="about__img">
                        <div class="about__img-shadow">

                        </div>
                    </div>
                    <div class="about__text">
                        <h5>Мягкие игрушки</h5>
                        <p>Милые игрушки для детей и взрослых</p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-3">
                <div class="about__card border">
                    <div class="about__img-wrap">
                        <img src="../assets/album/momLove.jpg" alt="" class="about__img">
                        <div class="about__img-shadow">

                        </div>
                    </div>
                    <div class="about__text">
                        <h5>Вкусные подарки</h5>
                        <p>Натуральный мёд, сыр и авторские лакомства ручной работы.</p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-3">
                <div class="about__card border">
                    <div class="about__img-wrap">
                        <img src="../assets/album/shirtGrass.jpg" alt="" class="about__img">
                        <div class="about__img-shadow">

                        </div>
                    </div>
                    <div class="about__text">
                        <h5>Одежда ручной работы</h5>
                        <p>Вязанные свитера, катанные варежки и тёплые шарфы</p>
                    </div>
                </div>
            </div>
            <div class="col-md-6 col-lg-3">
                <div class="about__card border">
                    <div class="about__img-wrap">
                        <img src="../assets/album/juvelry.jpg" alt="" class="about__img">
                        <div class="about__img-shadow">

                        </div>
                    </div>
                    <div class="about__text">
                        <h5>Авторские украшения</h5>
                        <p>Вязаные браслеты, яркая бижутерия и изделия с натуральными камнями</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.about {
    .about__card {
        position: relative;
    }

    .about__img-wrap {
        display: block;
        position: relative;
    }

    .about__img-shadow {
        position: absolute;
        width: 100%;
        height: 100%;
        left: 0;
        top: 0;
        background: linear-gradient(to top,
                rgba(0, 0, 0, 0.6),
                rgba(0, 0, 0, 0.1));
    }

    .about__text {
        position: absolute;
        bottom: 0;
        left: 0;
        padding: 10px 10px;
        width: 100%;
    }
}
</style>