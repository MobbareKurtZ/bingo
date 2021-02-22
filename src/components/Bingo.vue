<template>
<div class="boxes">
    <h1><span>DALTONZ</span> INTREZZEKLUBBENBINGO</h1>
    <button @click="slumpa()" v-if="test">Nya tal</button>
    <div class="headers"><span>B</span><span>I</span><span>N</span><span>G</span><span>O</span></div>
    <div class="grid">
        <div v-for="(box) in boxes" :key="box.id" :value="box.id" @click="clickBox(box.id)" :class="{clickad: box.tick}" class="box">
            <p>{{box.content}}</p>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Bingo',
    methods: {
        slumpa() {
            let numbers = new Set;
            let ar = [];
            while (numbers.size < this.content.length-1) numbers.add(Math.floor(Math.random() * this.content.length));
            ar = Array.from(numbers)
            console.log(ar)
            this.boxes.forEach((box, i) => {
                box.content = this.content[ar[i]];
            });
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
            test: false,
            content: [
                "Någon mot nominerar sig",
                "Mötet ajourneras",
                "Intrezzeklubben fuckar statistiken",
                "Intrezzeklubben gör rätt på statistiken",
                "Ztyret vet inte hur stadgarna funkar",
                "Någon har läst stadgarna på spårvagnen",
                "Gustav Olsson är bitter",
                "Någon blir ansvarsbefriad",
                "Revisorerna har gjort fel",
                "Ingen vill vara revisor",
                "Nominerad vet inte hur man ska svara på relevant fråga",
                "Hela sektionsmötet sätter igång coffeebreak",
                "Någon har inte muteat sig",
                "Ztyrets mic är kass",
                "Någon får bingo",
                "Jag fick 2 i rad",
                "Intrezzeklubben nailar en tweet",
                "Robin pratar för mycket",
                "Intrezzeklubben har liiit merch",
                "Jag donera till intrezzeklubbens sicka merch",
                "Någon dricker kaffe",
                "Någon dricker kebabte",
                "Intrezzeklubben har en jätteintrezzant kahoot",
                "Webbgruppen har inval",
                "Fler än 15 personer på mötet",
                "Intrezzeklubben dumdum",
                "Nominerad tackar nej",
                "“Kan ni se min skärm?”",
                "Någon ligger i sängen",
                "“Zåååååååg”",
                "Falkman dyker upp",
                "Falkman dyker inte upp",
                "Ztyret ändrar dagordningen",
                "Intrezzeklubben fuckar upp kahooten",
                "Hur många procent är det i flaggpunsch?",
                "Jag ångrar att vi valde in dessa till intrezzeklubben",
                "“kan ni höra mig?”",
                "Någon sitter i en mikro med en dammsugare i micken",
                "https://sv.wikipedia.org/wiki/Intresseklubben",
                "Gratis:)))"
            ],
            boxes: [{
                    id: 1,
                    tick: false,
                    content: null
                },
                {
                    id: 2,
                    tick: false,
                    content: null
                },
                {
                    id: 3,
                    tick: false,
                    content: null
                },
                {
                    id: 4,
                    tick: false,
                    content: null
                },
                {
                    id: 5,
                    tick: false,
                    content: null
                },
                {
                    id: 6,
                    tick: false,
                    content: null
                },
                {
                    id: 7,
                    tick: false,
                    content: null
                },
                {
                    id: 8,
                    tick: false,
                    content: null
                },
                {
                    id: 9,
                    tick: false,
                    content: null
                },
                {
                    id: 10,
                    tick: false,
                    content: null
                },
                {
                    id: 11,
                    tick: false,
                    content: null
                },
                {
                    id: 12,
                    tick: false,
                    content: null
                },
                {
                    id: 13,
                    tick: false,
                    content: null
                },
                {
                    id: 14,
                    tick: false,
                    content: null
                },
                {
                    id: 15,
                    tick: false,
                    content: null
                },
                {
                    id: 16,
                    tick: false,
                    content: null
                },
                {
                    id: 17,
                    tick: false,
                    content: null
                },
                {
                    id: 18,
                    tick: false,
                    content: null
                },
                {
                    id: 19,
                    tick: false,
                    content: null
                },
                {
                    id: 20,
                    tick: false,
                    content: null
                },
                {
                    id: 21,
                    tick: false,
                    content: null
                },
                {
                    id: 22,
                    tick: false,
                    content: null
                },
                {
                    id: 23,
                    tick: false,
                    content: null
                },
                {
                    id: 24,
                    tick: false,
                    content: null
                },
                {
                    id: 25,
                    tick: false,
                    content: null
                },
            ]
        };
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped lang="scss">
</style>
