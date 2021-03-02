<template>
    <div>
        <input type="checkbox" id="themeSwitch" name="theme-switch" class="theme-switch__input" /> 
            <label for="themeSwitch" class="theme-switch__label"> 
                <span></span> 
            </label>
        <main class="darkmode">
            <h2>Css Custom Properties Dark/Light Mode</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsa earum eum dicta eius minus voluptatibus odit, suscipit quidem similique
                consequuntur commodi nisi enim reiciendis porro consequatur eos blanditiis aspernatur ea.
            </p>
        </main>
    </div>
</template>

<style scoped>
 
.darkmode {
    --backgroundLight: rgb(255, 255, 255);
    --textLight: rgb(0, 0, 0);
    margin: var(--spacing-xlg);
    padding: calc(var(--spacing-xlg) * 1.5);
    border: 1px solid #ccc;
    border-radius: 0.3rem;
    box-shadow: 0 3px 4px rgba(0, 0, 0, 0.15);
}

main {
    --gradDark: #ecf8fa; 
    --gradLight: #bbbbbb; 
    background: linear-gradient(to bottom, var(--gradDark), var(--gradLight)); 
    padding: var(--spacing-md); 
    text-align: left;
}
.theme-switch__input:checked ~ main, 
.theme-switch__input:checked ~ label {
    --text: white;
}
.theme-switch__input:checked ~ main {
    --gradDark: var(--color); 
    --gradLight: #102128;
    --darken: 0.8;
    color: var(--text);
}
.theme-switch__input,
.theme-switch__label {
    position: absolute;
    z-index: 1;
}
.theme-switch__input {
    opacity: 0;
}
.theme-switch__input:hover + .theme-switch__label, 
.theme-switch__input:focus + .theme-switch__label {
    background-color: lightSlateGray;
}
.theme-switch__input:hover + .theme-switch__label span::after, 
.theme-switch__input:focus + .theme-switch__label span::after {
    background-color: #d4ebf2;
}
.theme-switch__label {
    padding: var(--spacing-md); 
    margin: var(--spacing-lg) var(--spacing-xxlg); 
    transition: background-color 200ms ease-in-out; 
    width: 79px; 
    height: 30px; 
    border-radius: 50px; 
    text-align: center; 
    background-color: slateGray; 
    box-shadow: -4px 4px 15px inset rgba(0, 0, 0, 0.4);
}
.theme-switch__label::before {
    right: 100%; 
    margin-right: var(--spacing-sm); 
}
.theme-switch__label::after {
    left: 100%; 
    margin-left: var(--spacing-sm); 
    color: lightSlateGray;
}
.theme-switch__label span {
    position: absolute; 
    bottom: calc(100% + 10px); 
    left: 0; 
    width: 100%;
}
.theme-switch__label span::after {
    position: absolute; 
    top: calc(10% + 15px); 
    left: var(--spacing-md); 
    width: 35px; 
    height: 35px; 
    content: ''; 
    border-radius: 50%; 
    background-color: lightBlue; 
    transition: transform 200ms, 
    background-color 200ms; 
}
.theme-switch__input:checked ~ .theme-switch__label {
    background-color: lightSlateGray;
}
.theme-switch__input:checked ~ .theme-switch__label::before {
    color: lightSlateGray;
}
.theme-switch__input:checked ~ .theme-switch__label::after {
    color: turquoise;
}
.theme-switch__input:checked ~ .theme-switch__label span::after {
    transform: translate3d(var(--spacing-xlg), 0, 0);
}

</style>