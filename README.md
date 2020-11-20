# Petitlavieve
HTML modules for use in the webshop.

## How to
In the JouwWeb editor, add a custom HTML block to the page.
The HTML block should contain an empty div for each module you need to import:
`css` for styling, `html` for the building blocks, 
and `js` or `ajax` for fancy functionalities.
These divs are then modified on page load by an Ajax `document.ready` function.
The function replaces the content of a div with a linked file hosted on GitHub.
This way, we can keep the custom HTML code on petitlavieve.nl simple and stable,
while developing the page contents in the Git repo.

Example:

```html
<div id="css-filter-checkboxes"></div>
<div id="html-filter-checkboxes-maatjes"></div>
<div id="js-filter-checkboxes-maatjes"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script>
  $(document).ready(function(){ 
    $('#css-filter-checkboxes').load("https://raw.githubusercontent.com/VanOverbeeke/petitlavieve/main/filters/css-filter-checkboxes.css.html");
    $('#html-filter-checkboxes-maatjes').load("https://raw.githubusercontent.com/VanOverbeeke/petitlavieve/main/filters/html-filter-checkboxes-maatjes.html");
    $('#js-filter-checkboxes-maatjes').load("https://raw.githubusercontent.com/VanOverbeeke/petitlavieve/main/filters/js-filter-checkboxes-maatjes.js.html");
  });
</script>
```
