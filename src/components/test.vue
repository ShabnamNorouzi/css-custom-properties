<template>
    <div class="container">
        <header class="column header"></header>
        <sidebar class="sidebar column">
        </sidebar>
        <div class="column content">
            <Cards />
        </div>
        <Footer class="footer column"></Footer>
    </div>

</template>

<script>
import Cards from './components/Cards.vue'

export default {
  name: 'App',
  components: {
    Cards
  }
}
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Merriweather:400,400i,700");

:root, [data-theme="default"] {
    --spacing-xs: 1px;
    --spacing-md: calc(var(--spacing-xs) * 10);
    --spacing-lg: calc(var(--spacing-xs) * 50);
    --spacing-xlg: calc(var(--spacing-xs) * 100);

    --font-primary: Merriweather, serif;
    --font-secondary: Georgia, serif;

    --text-scale-ratio: 1.2;
    --text-unit: 1rem;
    --text-xs: calc((var(--text-unit) / var(--text-scale-ratio)) / var(--text-scale-ratio));
    --text-sm: calc(var(--text-xs) * var(--text-scale-ratio));
    --text-md: calc(var(--text-sm) * var(--text-scale-ratio) * var(--text-scale-ratio));
    --text-lg: calc(var(--text-md) * var(--text-scale-ratio));
    --text-xl: calc(var(--text-lg) * var(--text-scale-ratio));

    --height-xs: 15px;
    --height-sm: calc(var(--height-xs) * 2.5);
    --height-md: calc(var(--height-xs) * 4);
    --height-lg: calc(var(--height-xs) * 82);
    --content-height: calc(var(--height-lg) - (var(--height-md) * 3));



    --primary-bg-color: hsla(180, 6%, 15%, 1);
    --secondary-bg-color: hsla(0, 0%, 66%, 1);
    --tertiary-color: #6a995e;

    --shadow-color: #CCCCCC;
    --text-color: hsla(0, 100%, 100%, 1);
    --border-color: hsla(0, 0%, 66%, 1);
}

[data-theme="dark"] {
    --primary-bg-color: hsla(0, 0%, 97%, 1);
    --secondary-bg-color: hsla(180, 6%, 15%, 1);
}


*, ::after, ::before {
    box-sizing:border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
    --columns: 12;
    display: flex;
    flex-wrap: wrap;
    font-family: var(--font-primary);
}

.column {
    --width: 0;
    background-color: rgb(58, 0, 10);
    border: 0.05px solid var(--border-color);
    flex-basis: calc(var(--width) / var(--columns) * 100%);
}

.navbar {
   --width: 12;  
   height: var(--height-md); 
   display: flex;
   align-items: center;
   background-color: var(--primary-bg-color);
   font-size: var(--text-xs);
   color: var(--border-color);
}

.content {
    --width: 10;
}

.header {
   --width: 12;  
   height: calc(var(--height-md) * 2);
}

.sidebar {
    --width: 3;
    height: var(--height-lg);
}

.footer {
    --width: 12;
    height: var(--height-xs);
}
</style>
