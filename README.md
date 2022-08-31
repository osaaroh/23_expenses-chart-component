# Frontend Mentor - Expenses chart component

![Design preview for the Expenses chart component coding challenge](./design/desktop-preview.jpg)

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the app depending on their device's screen size
- See hover states for all interactive elements on the page
- Generate a new piece of advice by clicking the dice icon


### Links

- Live Site URL: [Live Demo](https://expenses-chart-component-o.netlify.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Flexbox
- [Chart.js](https://www.chartjs.org/)


### What I learned

- Chart.js Library

```js
const ctx = document.querySelector("#spendingChart").getContext("2d");
const spendingChart = new Chart(ctx, {
    type: "bar",
    data: {
        labels: ["mon", "tue", "weds", "thu", "fri", "sat", "sun"],
        datasets: [{
            data: [17.45, 34.91, 52.36, 31.07, 23.39, 43.28, 25.48],
            backgroundColor: [
                "hsl(10, 79%, 65%)",
                "hsl(10, 79%, 65%)",
                "hsl(186, 34%, 60%)",
                "hsl(10, 79%, 65%)",
                "hsl(10, 79%, 65%)",
                "hsl(10, 79%, 65%)",
            ],
            hoverBackgroundColor: "hsl(10, 87%, 79%)",
            borderWidth: 1,
            borderRadius: 5,
        }, ],
    },
    options: {
        plugins: {
            legend: {
                display: false,
            },
            tooltip: {
                caretSize: 0,

                bodyFont: {
                    size: 15,
                },
                padding: 10,
                displayColors: false,
                backgroundColor: "rgba(56, 35, 20,0.9)",
                yAlign: "bottom",
                callbacks: {
                    title: function() {},
                    label: function(context) {
                        return "$" + context.formattedValue;
                    },
                },
            },
            fillStyle: "red",
        },
        scales: {
            x: {
                ticks: { display: true },
                grid: {
                    display: false,
                },
            },
            y: { ticks: { display: false }, grid: { display: false } },
        },
    },
});

```


## Author
- Frontend Mentor - [@Master-Osaro](https://www.frontendmentor.io/profile/master-osaro)
- Twitter - [@iyoha_osaro](https://www.twitter.com/yourusername)


**Really had fun building!** 🚀
