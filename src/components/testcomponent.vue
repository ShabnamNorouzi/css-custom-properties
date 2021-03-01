<template>
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 60 60" width="0" height="0"><defs><g id="arrow"><path d="M30 0C13.4 0 0 13.4 0 30s13.4 30 30 30 30-13.4 30-30S46.6 0 30 0zm9.5 41.6l-2.1-2.2 8.3-7.9H8v-3h37.8l-8.3-7.9 2.1-2.2L51.7 30 39.5 41.6z"/></g></defs></svg>
    <div class="wrapper">
        <article class="card card--event">
            <a class="card__link" href="https://www.meetup.com/wpbristol/"></a>
            <div class="card__content">
                <h3>March 5</h3>
                <a class="card__heading" href="https://www.meetup.com/wpbristol/">
                    <h2>Total Orders</h2>
                </a>
                <p>We meet monthly for interesting talks.</p>
                <svg class="card__icon" viewBox="0 0 60 60" width="60" height="60">
                    <use href="#arrow"/>
                </svg>
            </div>
        </article>

        <article class="card">
            <a class="card__link" href="https://css-irl.info/becoming-a-tech-speaker/"></a>
            <div class="card__content">
                <h3>February 23</h3>
                <a class="card__heading" href="https://css-irl.info/becoming-a-tech-speaker/">
                    <h2>Daily Sales</h2>
                </a>
                <p>How becoming a tech speaker has helped me develop my career and my confidence in myself as a developer, and why you should try it!</p>
                <svg class="card__icon" viewBox="0 0 60 60" width="60" height="60">
                    <use href="#arrow"/>
                </svg>
                </div>
        </article>
        
        <article class="card">
            <a class="card__link" href="https://css-irl.info/to-grid-or-to-flex/"></a>
            <div class="card__content">
                <h3>February 11</h3>
                <a class="card__heading" href="https://css-irl.info/to-grid-or-to-flex/">
                    <h2>To Grid or to Flex?</h2>
                </a>
                <p>How do you know which layout method to choose? Here are some pointers</p>
                <svg class="card__icon" viewBox="0 0 60 60" width="60" height="60">
                    <use href="#arrow"/>
                </svg>
                </div>
        </article>
    </div>
</template>

<script>
export default {
  name: 'Cards',
  props: {
    msg: String
  }
}
</script>

<style scoped >
@import url("https://fonts.googleapis.com/css?family=Lato:400,400i,700");

* {
	box-sizing: border-box;
}

body {
  font-family: Lato, sans-serif;
  background-color: #212121;
}
a {
  text-decoration: none;
  color: black;
}
p {
  line-height: 1.5;
}
.wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
.card {
  --hue: 259;
  --rotation: 180;
  --hueComplementary: calc(var(--hue, 20) + var(--rotation, 0));
  --th: hsl(var(--hue), 72%, 64%);
  --thDark: hsl(var(--hue), 72%, 28%);
  --thLight: hsl(var(--hue), 72%, 84%);
  --accent: hsl(var(--hueComplementary, var(--hue)), 72%, 64%);
  position: relative;
  margin: 20px;
  flex: 0 1 350px;
  box-shadow: 0.2em 0.2em 20px rgba(0, 0, 0, 0.9);
  border-radius: 0.2em;
  color: var(--thDark);
}
.card h2 {
  color: var(--thDark);
  margin-bottom: 10px;
  padding-right: 40px;
  font-size: 1.65rem;
}
.card h3 {
  background: linear-gradient(45deg, var(--thDark), var(--th));
  color: var(--thLight);
  padding: 5px 10px;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  margin: 0;
  font-size: 1rem;
  border-radius: 0.2em 0.2em 0 0;
}
.card p {
  padding-right: 40px;
  margin-bottom: 30px;
}
.card time {
  font-weight: normal;
}
.card time::before {
  content: '|';
  margin: 0 0.5em;
}
.card__content {
  background: linear-gradient(30deg, var(--th), var(--thLight));
  padding: 50px 30px 20px;
  height: 100%;
  display: flex;
  flex-direction: column;
  border-radius: 0.2em;
}
.card__content::after {
  opacity: 0;
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  transition: opacity 200ms;
  background: var(--accent);
  pointer-events: none;
}
.card__link {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: block;
}
.card__link:hover + .card__content::after, .card__link:focus + .card__content::after {
  opacity: 1;
}
.card__link:hover + .card__content .card__icon, .card__link:focus + .card__content .card__icon {
  color: var(--th);
}
.card__icon {
  margin-top: auto;
  fill: currentColor;
  width: 40px;
  align-self: flex-end;
  color: var(--accent);
  position: relative;
  z-index: 1;
  transition: color 200ms;
  pointer-events: none;
}
.card--event {
  --hue: 180;
}

</style>
