<template>
    <div class="cards">
        <input type="radio" id="yellow" name="colors" checked>
        <label for="yellow"></label>
        <input type="radio" id="pink" name="colors" checked>
        <label for="pink"></label>
        <div class="cards-wrapper">
            <div class="card">
                <div class="image"></div>
                <div class="text">
                    <h5 class="title with-tag"></h5>
                    <span class="tag"></span>
                    <span class="tag"></span>
                    <span class="tag"></span>
                    <div class="paragraph color-gray">
                        <p></p>
                        <p></p>
                        <p></p>
                        <p></p>
                        <p></p>
                    </div>
                    <div class="divider">
                        <button><span></span></button>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="image"></div>
                <div class="text">
                    <h5 class="title with-tag"></h5>
                    <span class="tag"></span>
                    <span class="tag"></span>
                    <span class="tag"></span>
                    <div class="paragraph color-gray">
                        <p></p>
                        <p></p>
                        <p></p>
                        <p></p>
                        <p></p>
                    </div>
                    <div class="divider">
                        <button><span></span></button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>



<style scoped>
:root {
    --colorMain: #444;
    --colorLight: #999;
    --colorAccent: #ddd;
}

[type="radio"] {
    display: none;
}
label {
    display: inline-block;
    width: 30px;
    height: 30px;
    margin: 10px;
    border-radius: 50%;
    box-shadow: 0 0 0 2px #f9f9f9, 0 0 0 3px #ddd;
    cursor: pointer;
}

[type="radio"]:checked + label {
    box-shadow: 0 0 0 2px #f9f9f9, 0 0 0 3px var(--colorMain);
}

#yellow + label {
    background: #ffd94e;
}

#yellow:checked ~ .cards-wrapper,
#yellow:checked + label {
    --colorMain: #ffd94e;
    --colorLight: #ffe37e;
    --colorAccent: #ffedae;
}

#pink + label {
    background: #ffa1ad;
}

#pink:checked ~ .cards-wrapper,
#pink:checked + label {
    --colorMain: #ffa1ad;
    --colorLight: #ffc3ca;
    --colorAccent: #ffdce1;
}

.cards-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    padding: 30px;
}

.card {
    flex: 1;
    background: #fff;
    padding: 23px 20px;
    border-radius: 4px;
    margin: 10px;
    position: relative;
    overflow: hidden;
    text-align: left;
    max-width: 260px;
}
.card:before {
    content: "";
    position: absolute;
    height: 6px;
    width: 100%;
    top: -1px;
    left: 0;
    background: var(--colorMain);
}
.image {
    background: var(--colorLight);
    background: linear-gradient(
    to bottom right,
    var(--colorLight),
    var(--colorAccent)
    );
    width: 100%;
    height: 140px;
    border-radius: 3px;
}
.title {
    margin: 20px 0;
    background: var(--colorMain);
    height: 25px;
    width: 85%;
    border-radius: 20px;
}
.title.with-tag {
    margin: 20px 0 10px;
}
.tag {
    width: 45px;
    height: 10px;
    display: inline-block;
    margin-right: 8px;
    border-radius: 20px;
    background: var(--colorAccent);
}
.divider {
    border-top: 1px solid #eee;
    padding-top: 20px;
}
button {
    border-radius: 30px;
    background: var(--colorMain);
    border: none;
    border: 4px solid var(--colorMain);
    width: 100%;
    padding: 15px;
    text-align: center;
}
button span {
    width: 40%;
    height: 8px;
    background: #fff;
    display: inline-block;
    border-radius: 20px;
}
.paragraph {
    margin: 20px 0;
}
.paragraph p {
    width: 90%;
    background: #ddd;
    height: 15px;
    margin: 0 0 12px;
    border-radius: 20px;
}
.paragraph p:nth-child(2n + 2) {
    width: 80%;
}
.paragraph p:last-child {
    width: 40%;
}
</style>
