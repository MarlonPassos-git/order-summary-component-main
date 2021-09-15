# order-summary-component-main

![Farmers Market Finder Demo](Animação.gif)

## The challenge

- Develop a page trying to make it as close as possible to the image made by the designer
- View focus states for interactive elements
- That the page is responsive to screens between 280px and +1920px wide

## Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [https://marlonpassos-git.github.io/order-summary-component-main/](https://marlonpassos-git.github.io/order-summary-component-main/)
  

## Built with

- SASS 
- HTML 

## What I learned

- I found that to create 100% flexible elements from start to finish in their dimensions it's good to define the maximum and minimum size, and in the size value we define a percentage of the available screen. 
  ```
    max-width: 450px;
    max-height: 220px;
    min-height: 160px;
    height: 45vw;
  ```
  So I didn't even have to use `@media`, and there wasn't that weird thing about changing the size of an element drastically from one pixel to another either.

  To find out the percentage used in VW I created this function

  ```
  function porcentage(elementMinimuSize, screenMinimumSize) {

    const list = new Set()

    for (let i = screenMinimumSize ; i < screenMinimumSize + 10; i++) {
        for (let j = 0; j < 100 ;j++) {

            let size = Math.trunc(i * (j * 0.01)) 

            if (elementMinimuSize == size) list.add(j) 
        }

    }
    let listArry = Array.from(list)    
    
    return listArry[listArry.length - 1]
  }


  porcentage(160, 350) // 45px
  ```
  In the end this means that on average when my screen is **350px** wide my image will be **160px** high using **45vw** as my element height
  
- I learned how to use Gifs in README.md to make things more beautiful and intuitive. Along with that I discovered a beautiful program that does this [Screen To Gif](https://www.screentogif.com/). It is free, and allows us to record our screen and return a gif easily, it contains many other settings that I know will be useful in the future. 



## **Author**

- Frontend Mentor - [@MarlonPassos-git](https://www.frontendmentor.io/profile/MarlonPassos-git)


