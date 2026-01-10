<template>
    <div><canvas id="snow" /></div>
</template>

<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    mounted() {
        const canvas = document.getElementById("snow");
        const ctx = canvas.getContext("2d");

        let width, height;
        let flakes = [];
        const FLAKE_COUNT = 150;

        function resize() {
            width = canvas.width = window.innerWidth;
            height = canvas.height = window.innerHeight;
        }
        window.addEventListener("resize", resize);
        resize();

        class Snowflake {
            constructor() {
                this.reset();
                this.y = Math.random() * height;
            }

            reset() {
                this.x = Math.random() * width;
                this.y = -10;
                this.r = Math.random() * 3 + 1;
                this.speed = Math.random() * 1.5 + 0.5;
                this.wind = Math.random() * 0.5 - 0.25;
                this.opacity = Math.random() * 0.6 + 0.3;
            }

            update() {
                this.y += this.speed;
                this.x += this.wind;

                if (this.y > height) this.reset();
                if (this.x > width) this.x = 0;
                if (this.x < 0) this.x = width;
            }

            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.r, 0, Math.PI * 2);
                ctx.fillStyle = `rgba(255,255,255,${this.opacity})`;
                ctx.fill();
            }
        }

        function init() {
            flakes = [];
            for (let i = 0; i < FLAKE_COUNT; i++) {
                flakes.push(new Snowflake());
            }
        }

        function animate() {
            ctx.clearRect(0, 0, width, height);

            for (const flake of flakes) {
                flake.update();
                flake.draw();
            }

            requestAnimationFrame(animate);
        }

        init();
        animate();
    },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#snow {
    position: fixed;
    inset: 0;
    pointer-events: none;
    z-index: 10;
}
</style>
