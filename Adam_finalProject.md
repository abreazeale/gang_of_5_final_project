# Adam Final Project

## HTML File links
+ <https://github.com/abreazeale/gang_of_5_final_project/blob/master/adamfinal/adamfinal.html>
+ <https://github.com/abreazeale/gang_of_5_final_project/blob/master/adamfinal/adamcalc.html>
+ <https://github.com/abreazeale/gang_of_5_final_project/blob/master/adamfinal/adamform.html>
+ <https://github.com/abreazeale/gang_of_5_final_project/blob/master/adamfinal/adamapi.html>

## AJAX Calls
I am doing two AJAX calls in this site, one GET and one POST:
### GET
The GET call is against my Node server and is retrieving data from a JSON file in the adamfinal folder:
```
function testNodeGet(){
   $.getJSON("http://127.0.0.1:8080/getMortality", function(data, status, xhr){
             DisplayJSONobjectArrayAsTable(data, "myTable");
            })};
```
### POST
The POST call is against the USA Spending API, specifically the ```/api/v2/federal_accounts/```
```
function testNodePost(){
    ajaxSetting = getDefaultAjaxSettings();
    ajaxSetting.method = "POST";
    ajaxSetting.contentType = "application/json";
    ajaxSetting.url = "https://api.usaspending.gov/api/v2/federal_accounts/";
            ajaxSetting.data = "{\"agency\": 14}";
    ajaxSetting.success =  function (data, status, xhr) {
        console.log(status);

        DisplayJSONobjectArrayAsTable(data, "myTable");
        let responseHeaders = xhr.getAllResponseHeaders();
        //   let responseHeader = xhr.getResponseHeader();
        let responseText = xhr.responseText;
        let responseCode = xhr.status;
        let statusText = xhr.statusText;
    }
    jQuery.ajax(ajaxSetting);
}
```

## Lessons Learned
+ CORS can be a real pain!
+ Controlling Type within JS is difficult

## "Live" Site URL
