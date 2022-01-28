<template>
    <div class="task">
        <div class="w3-card">
            <h1 class="task-title">title</h1>

            <div class="task-progression w3-border">
                <div id="progress-bar" class="w3-green" :style="'height: 24px;' + ' width: ' + width + '%'"></div>
                <div class="btn-container">
                    <button value="0" @click="move($event)" class="btn w3-btn" id="progress0">0%</button>
                    <button value="25" @click="move($event)" class="btn w3-btn" id="progress25">25%</button>
                    <button value="50" @click="move($event)" class="btn w3-btn" id="progress50">50%</button>
                    <button value="75" @click="move($event)" class="btn w3-btn" id="progress75">75%</button>
                    <button value="100" @click="move($event)" class="btn w3-btn" id="progress100">100%</button>
                </div>
            </div>

            <div class="task-commentary">commentaire</div>

            <button class="task-btn w3-btn w3-red">SUPPRIMER</button>
            <button class="task-btn w3-btn w3-blue">METTRE EN PASE</button>
            <button class="task-btn w3-btn w3-green">terminé</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'taskCard',
    data() {
        return {
            width: 1,
        };
    },
    methods: {
        /*  changeProgress(e) {
            var progressBar = document.getElementById('progress-bar');
            console.log('width: ' + e.target.value + ';');

            progressBar.style.width = 'width: ' + e.target.value + ';';
        }, */
        move(e) {
            var valueX1 = e.target.value * 1;
            var elem = document.getElementById('progress-bar');
            var width = this.width;
            console.log(valueX1);
            console.log(e.target.value);
            console.log('fsefsefsefse', this.width);
            var id = setInterval(frame, 10);
            function frame() {
                if (width > valueX1) {
                    clearInterval(id);
                } else {
                    width++;
                    console.log('tw', this.width);
                    this.width = width;
                }
                console.log('tw', this.width);
                elem.style.width = this.width + '%';
            }
        },
    },
};
</script>

<style lang="scss" scoped>
.task {
    width: 350px;
    border: 1px solid blue;
    &-btn {
        width: 100%;
    }
    &-title {
        width: 100%;
        font-size: 50px;
    }
    &-progression {
        width: 100%;
    }
    &-commentary {
        width: 100%;
    }
}
.btn-container {
    display: flex;
    justify-content: center;
}
</style>
