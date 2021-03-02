<template>
    <div id="app">
        <div class="container">
            <div class="header column">
                <input type="range" min="0" max="360" step="1" id="hue" @input="updateTheme">
                <label class="lable" for="hue">Change The Theme: {{ hueValue }} </label>
            </div>
            <header class="header column">
                <div class="container">
                    <a href="" class="item item-prev">Home</a>
                    <a href="" class="item item-main">Search</a>
                    <a href="" class="item item-next">Contact</a>
                </div>
            </header>
            <main class="content column">
                <cards />
                <darkMode />
            </main>
            <aside class="sidebar column">
            </aside>
            <footer class="footer column">Footer</footer>
        </div>
    </div>
</template>

<script>
import cards from './components/cards.vue'
import darkMode from './components/darkMode.vue'

export default {
    name: 'App',

    data() {
        return {
            hueValue: 180
        }
    },

    methods: {

        updateTheme(event) {
            const value = event.target.value;
            this.hueValue = value;
            document.documentElement.style.setProperty('--hue', this.hueValue);
        }
    },

    components: {
        cards,
        darkMode
    }
}


</script>

<style>
    @import './css/css-custom.css';

</style>
