# Nigerian States and their LGAs in json format
You can use this json to load values for states and their lgas into you application or website.

The most popular use being "State of Origin" and LGA form fields

simply copy the `states.json` file into your project and import it into your `js` file and you're good to go

Eg: Using this data to populate a select field with states options
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <select id="states"></select>
</body>
</html>
```

in your js file...
```js
import * as states from 'path/to/states.json'
import $ from 'jquery';

let statesField = $('#states');

for (state in states) {
    statesField.append(`<option value="${state.name}">${state.name}</option>`);
}
```

Your html should look like this when you open it in your browser's devtools
```html
...
<body>
    <select id="states">
        <option value="Abia">Abia</option>
        ...
        <option value="Zamfara">Zamfara</option>
    </select>
</body>
```

If you're interested in how i scraped and prepared this data, read my article [here](https://jeffreyon.hashnode.dev/heres-a-big-fat-list-of-nigerian-states-and-their-lgas-in-json-for-your-projects)
