# Petitlavieve
HTML modules for use in the webshop.

## How to use
In the JouwWeb editor, add the `Embed Code` block to the page.
Click the newly added block and click the `Embed aanpassen` button.
Go to the tab `Eigen HTML` and paste the template shown below.
Adjust the URL inside the Ajax code to select the module you want to load.

Template:

```html
<div id="filter-checkboxes-maatjes"></div>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
<script>
  $(document).ready(function(){
    $('#filter-checkboxes-maatjes').load("https://raw.githubusercontent.com/VanOverbeeke/petitlavieve/main/filters/filter-checkboxes-maatjes-all.html");
  });
</script>
```

## How it works
The custom HTML block creates an empty div on the pages and fills it with content after the page loads.
The content to use is hosted on github.com/VanOverbeeke and is linked to inside the Ajax script block.
Each custom block used on `petitlavieve.nl` is defined in the github repository.
The example shown above loads the checkboxes to filter products on the page by `Maat`.

The script referred to in the example, `filters/filter-checkboxes-maatjes-all.html`, 
in turn loads multiple other scripts in the same way
`css` for styling, `html` for the page elements, 
and `js` or `ajax` for fancy functionalities.
For other pages, just adjust the url you use in the JouwWeb editor
to load the custom block you need from the repo on github.com.

## But why?
The custom HTML code saved on petitlavieve.nl is minimal.
We can edit the website appearance without needing the JouwWeb editor.
We can use Git and version control to backup our page contents.
We can play around with new developments, and revert to a 'safe' version at any time.
