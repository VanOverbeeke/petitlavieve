# Petitlavieve
HTML modules for use in the webshop.

## How to
In the JouwWeb editor, add a custom HTML block to the page.
Paste the template shown below in the custom HTML editor.
This block creates an empty div on the pages and fills it with content after the page loads.
The content to use is hosted on github.com/VanOverbeeke and is linked to inside the Ajax script block.
Each custom block used on `petitlavieve.nl` is defined in the github repository.
This example loads the checkboxes to filter products on the page by `Maat`:

```html
<div id="filter-checkboxes-maatjes"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script>
  $(document).ready(function(){
    $('#filter-checkboxes-maatjes').load("https://raw.githubusercontent.com/VanOverbeeke/petitlavieve/main/filters/filter-checkboxes-maatjes-all.html");
  });
</script>
```

The script referred to here, `filters/filter-checkboxes-maatjes-all.html`, 
in turn loads multiple other scripts in the same way
`css` for styling, `html` for the page elements, 
and `js` or `ajax` for fancy functionalities.
For other pages, just adjust the url you use in the JouwWeb editor
to load the custom block you need from the repo on github.com.

This way, we can keep the custom HTML code on petitlavieve.nl simple and stable,
while developing the page contents in the Git repo.
