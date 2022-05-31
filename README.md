# Learning CSS Grid

## CSS Grid Slides

## Code

### 1

```css
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

body {
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    line-height: 1.5;
    color: #333;
    background: #f5f5f5;
}

.container {
    max-width: 960px;
    margin: 100px auto;
    padding: 10px;
    display: grid;
    /*grid-template-columns: 1fr 3fr 2fr;*/
    grid-template-columns: repeat(3, 1fr);
    /*grid-template-columns: repeat(3, 100px);*/
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
    /*column-gap: 10px;*/
    /*row-gap: 5px;*/

    /*grid-auto-rows: 200px;*/
    /*grid-auto-rows: minmax(100px, auto);*/

    /*grid-template-rows: 200px 100px 200px;*/
    /*grid-template-rows: repeat(3, 1fr);*/

    /*align-items: stretch;*/
    /*align-items: start;*/
    /*align-items: center;*/
    /*align-items: end;*/

    justify-content: end;
}

.item {
    background: steelblue;
    color: #fff;
    padding: 20px;
    border: skyblue 1px solid;
}

/*.item:nth-of-type(2) {*/
/*    height: 100px;*/
/*    width: 100px;*/

/*    align-self: center;*/
/*    justify-self: center;*/
/*}*/

/*.item:nth-of-type(1) {*/
/*    background: black;*/
/*    !*grid-column-start: 1;*!*/
/*    !*grid-column-end: 3;*!*/
/*    !*Same*!*/
/*    grid-column: 1 / 3;*/
/*    !*Same*!*/
/*    !*grid-column: 1 / span 2;*!*/
/*}*/

/*.item:nth-of-type(3) {*/
/*    background: #333;*/
/*    grid-row: 2 / 4;*/
/*}*/

/*.item:nth-of-type(4) {*/
/*    background: #333;*/
/*    grid-row: 2 / 4;*/
/*}*/

@media (max-width: 700px) {
    .container {
        grid-template-columns: 1fr;
    }
}
```

### 2

```css
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

body {
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    /*line-height: 1.5;*/
    color: #333;
    background: #f5f5f5;
    display: grid;
    height: 100vh;
    grid-template-areas:
    'header header header'
    'nav content sidebar'
    'nav footer footer';
    grid-template-columns: 1fr 4fr 1fr;
    grid-template-rows: 80px 1fr 70px;
}

header, main, nav, aside, footer {
    background-color: steelblue;
    color: white;
    padding: 20px;
    border: skyblue 1px solid;
}

header {
    grid-area: header;
}

nav {
    grid-area: nav;
}

main {
    grid-area: content;
}

aside {
    grid-area: sidebar;
}

footer {
    grid-area: footer;
}
```

### 3

```css
* {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}

body {
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    line-height: 1.5;
    color: #333;
    background: #f5f5f5;
}

.testimonials {
    max-width: 1440px;
    margin: 100px auto;
    padding: 20px;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    /*grid-template-rows: repeat(2, 1fr);*/
    gap: 10px;
}

.card {
    background: #fff;
    border-radius: 10px;
    padding: 30px;
    margin-bottom: 10px;
}

.card__header {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
}

.card__header h3 {
    font-size: 15px;
}

.card__header p {
    opacity: 50%;
}

.card__image {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    border: 2px solid #996ed9;
    margin-right: 10px;
}

.card__lead {
    font-size: 1.5em;
    font-weight: 500;
    line-height: 1.3;
    margin-bottom: 20px;
}

.card__quote {
    font-size: 15px;
    font-weight: 500;
    line-height: 1.4;
    margin-bottom: 20px;
    opacity: 70%;
}

.card--bg-purple {
    background: blueviolet;
    color: white;

}

.card--bg-gray-blue {
    background: darkslategray;
    color: white;
}

.card--bg-black {
    background: #333333;
    color: white;
}

.card:nth-of-type(1) {
    grid-column: 1/ 3;
}

.card:nth-of-type(5) {
    grid-column: 2 / 4;
    grid-row: 2;
}

.card:nth-of-type(3) {
    grid-column: 4 / 5;
    grid-row: 1 / span 2;
}

.footer {
    text-align: center;
}

@media (max-width: 768px) {
    .testimonials {
        grid-template-columns: 1fr;
        width: 100%;
    }

    .card:nth-of-type(1) {
    grid-column: 1;
    }

    .card:nth-of-type(5) {
        grid-column: 1;
        grid-row: 4;
    }

    .card:nth-of-type(3) {
        grid-column: 1;
        grid-row: 3;
    }
}

```


## Credits

- [youtube | CSS Grid Crash Course 2022](https://www.youtube.com/watch?v=0xMQfnTU6oo&t=175s)
