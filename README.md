# Tablesorter

==============================================================================================

## View Helpers

    sortable_column_headings(columns, options={})

so

    <tr>
      <%= sortable_column_headings(['name', 'age']) %>
    </tr>

gives

    <tr>
      <th><a href="?dir=asc&sort=name">Name<span></span></a></th>
      <th><a href="?dir=asc&sort=age">Age<span></span></a></th>
    </tr>

When selected the link will be given a class of selected and either asc or desc.
You can use this to style the span with an arrow.

## Styling

If you want different headings to be displayed in your table headings use translations under the tablesorter namespace.

    en:
      tablesorter:
        age: 'Age (in years)'

## Active Record
tablesort method

    table_sort(sort_attr, dir, default_attr, default_dir)

eg 

    Person.scoped.table_sort(params[:sort], params[:dir], 'id', 'asc')

This project uses the MIT-LICENSE.

## TODO
* Test!
* Add a note about translations for table headings
* maybe extend api of helper method so you can pass a hash rather then an array
* Improve readme and add some default css to show arrow styling
* twitter bootstrap arrows option 
* Secondary sort
* Dont call order if no params passed
* mongoid?
* datamapper?
