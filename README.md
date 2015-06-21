## Website Performance Optimization portfolio project

Your challenge, if you wish to accept it (and we sure hope you will), is to optimize this online portfolio for speed! In particular, optimize the critical rendering path and make this page render as quickly as possible by applying the techniques you've picked up in the [Critical Rendering Path course](https://www.udacity.com/course/ud884).

### Getting started

####How to run

1. local
    ```bash
    cd /path/to/your-project-folder
    python -m SimpleHTTPServer 8080
    ```

1. to make local server accessible remotely
    ``` bash
    sudo ngrok http 8080
    ```

####Grunt taks

1. minifyHtml task

    ``` bash
    grunt minifyHtml
    ```

1. pagespeed ngrok task

    ``` bash
    grunt psi-ngrok
    ```

### Optimizations

####Part 1: Optimized PageSpeed Insights score for index.html
- web Font removed, cause a render-blocking in pagespeed
- added small Css in html>style to reduce the number of resources
- adding media="print" attribute in link stylesheet
- reduced images size and resolution

####Part 2: Optimized Frames per Second in pizza.html

- querySelector replaced with getElementById
- querySelectorAll replaced with getElementsByClassName
- improved performance for changePizzaSizes function
- collecting dom elements outside loop, if possible
- variables declaration outside of loops, if possible
- adding "tranform property" instead of "left property" in updatePositions function to move background pizzas
- calculate background Pizzas based of window width and height