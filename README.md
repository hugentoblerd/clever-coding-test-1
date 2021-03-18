# clever-coding-test

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).

## Tasks

- [x] Create a single page app.  On the top of the page create a centered header that says.  "The selected number is {{selectedNumber}}"

- [x] Below it I want you to create a responsive grid lay out of the numbers 1-100.  On mobile size screens it would display less numbers per row, a medium width screen it would show a little more and on a larger screen it would show the most numbers per row.

- [x] When a number is clicked on the header will change to show the reactive variable “selectedNumber”.  For example if you click on 5 the header will say.  "The select number is 5"

- [x] Bonus points make each grid item (individual numbers) a separate component and then pass in the number as a property of the grid item.  When the grid item is clicked communicate with the main page/component to reactively update the header with the number of the grid item that was clicked on.

- [x] Have the selected number grid item display with a color border around it setting it apart from the other grid items.
