<template>
<div class="boxes">
    <h1>DALTONZBINGO</h1>
    <div class="headers"><span>B</span><span>I</span><span>N</span><span>G</span><span>O</span></div>
    <div class="grid">
        <div v-for="(box, i) in boxes" :key="box.id" :value="box.id" @click="clickBox(box.id)" :class="{clickad: box.tick}" class="box">
            <h2>{{random[i]}}</h2>
        </div>
    </div>
    <button @click="slumpa()">Nya tal</button>
</div>
</template>

<script>
export default {
    name: 'Bingo',
    methods: {
        slumpa() {
            let numbers = new Set;
            let a1, a2, a3, a4, a5;
            let ar = [];
            while (numbers.size < 5) numbers.add(Math.floor(Math.random() * 14 + 1));
            a1 = Array.from(numbers)
            numbers = new Set;
            while (numbers.size < 5) numbers.add(Math.floor(Math.random() * 14 + 15));
            a2 = Array.from(numbers)
            numbers = new Set;
            while (numbers.size < 5) numbers.add(Math.floor(Math.random() * 14 + 30));
            a3 = Array.from(numbers)
            numbers = new Set;
            while (numbers.size < 5) numbers.add(Math.floor(Math.random() * 14 + 45));
            a4 = Array.from(numbers)
            numbers = new Set;
            while (numbers.size < 5) numbers.add(Math.floor(Math.random() * 14 + 60));
            a5 = Array.from(numbers)
            ar = ar.concat(a1, a2, a3, a4, a5);
            this.random = ar;
        },
        clickBox(id) {
            this.boxes[id - 1].tick = !this.boxes[id - 1].tick;
            this.check(id);
        },
        check(id) {
            for (let i = 0; i < 5; i++) {
                this.boxes[id - 1];
            }
        }
    },
    created() {
        this.slumpa();
    },
    data() {
        return {
            random: [],
            boxes: [{
                    id: 1,
                    tick: false
                },
                {
                    id: 2,
                    tick: false
                },
                {
                    id: 3,
                    tick: false
                },
                {
                    id: 4,
                    tick: false
                },
                {
                    id: 5,
                    tick: false
                },
                {
                    id: 6,
                    tick: false
                },
                {
                    id: 7,
                    tick: false
                },
                {
                    id: 8,
                    tick: false
                },
                {
                    id: 9,
                    tick: false
                },
                {
                    id: 10,
                    tick: false
                },
                {
                    id: 11,
                    tick: false
                },
                {
                    id: 12,
                    tick: false
                },
                {
                    id: 13,
                    tick: false
                },
                {
                    id: 14,
                    tick: false
                },
                {
                    id: 15,
                    tick: false
                },
                {
                    id: 16,
                    tick: false
                },
                {
                    id: 17,
                    tick: false
                },
                {
                    id: 18,
                    tick: false
                },
                {
                    id: 19,
                    tick: false
                },
                {
                    id: 20,
                    tick: false
                },
                {
                    id: 21,
                    tick: false
                },
                {
                    id: 22,
                    tick: false
                },
                {
                    id: 23,
                    tick: false
                },
                {
                    id: 24,
                    tick: false
                },
                {
                    id: 25,
                    tick: false
                },
            ]
        };
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped lang="scss">
</style>
