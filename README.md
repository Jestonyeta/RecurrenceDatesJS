## Usage
```html
<!DOCTYPE HTML>
<html>
  <head>
    <title>RecurrenceDatesJS</title>
    <script src="RCD.js"></script>
  </head>
  <body>
    <script>
    let rcd = new RCD({
       weekdays:['mo','we','su'],
       start_date:'16/01/2022',
       end_date:'16/12/2024',
       freq:'w',
       interval:1
    });
    let res = rcd.results();
    if(res.error){
       alert(res.error);
    }else{
       console.log(res.dates);
       // do something
    }
    </script>
  </body>
</html>
```
## Properties & Values
| Option   | Type | Value | Required | Default |
| ---      | ---       | --- | --- | --- |
| <code>weekdays</code> | Array    | ["su","mo","tu","we","th","fr","sa"] | Optional |  All |
| <code>freq</code>     | String       | w, m, y, 1wm, 2wm, 3wm, 4wm, jan, feb, mar, apr, may, jun, jul, aug, sep, oct, nov, dec | Optional | w |
| <code>interval</code> | Integer | 1, 2, 3, 4, 5 | true | |
|<code>start_date</code>|String|DD/MM/YY|true| |
|<code>end_date</code>|String|DD/MM/YY|true| |
## Response
| Key | Type |
| ---   | ---  | 
| error | String | 
| dates | Array |
