# Date_counting_back_and_forwards
# javasript. Node.js


Count date backwards or forwards.

Here we count date backwards 12 days from today's date.

Keyword : date.setDate(-12);  Or 12 to move forwards.

```
var date = new Date();
console.log("Today's Date: " + date + "</b><br>" );
date.setDate(-12);
console.log ( "The day we get after subtracting is: " + date); 
     
```

Output
```
Today's Date: Wed Mar 01 2023 13:34:23 GMT+0530 (India Standard Time)</b><br>
The day we get after subtracting is: Thu Feb 16 2023 13:34:23 GMT+0530 (India Standard Time)

```
![image](https://user-images.githubusercontent.com/14288989/222081460-c7ca65e7-56f9-42d8-aec6-8df17386b89e.png)


```
shashi@shashiraspberrypi:~/javascripts_dir $ cat countdate.js 
var date = new Date();
console.log("Today's Date  : " + date + "</b><br>" );
//console.log("Today's String: " + date.toString() + "</b><br>" );

let result = convert_date_to_string ( date);
console.log ( "Today's date  "+ result );

result = convert_date_to_string( new Date(date.setDate(-20)) );
console.log ("20 days ago" + result );

function convert_date_to_string( date_to_convert ){
	var year  = date_to_convert.getFullYear(); // 2023
	var month = date_to_convert.getMonth()+1; // 3
	var day  = date_to_convert.getDate(); 

	month = month.toString().padStart(2,"0");
	day   = day.toString().padStart(2,"0");; 

        let result_to_return = year.toString().concat("-").concat(month).concat("-").concat(day.toString());

	return result_to_return;
}
```



Output :

```
Today's Date  : Wed Mar 01 2023 17:30:11 GMT+0530 (India Standard Time)</b><br>
Today's date  2023-03-01
20 days ago.  2023-02-08
```
