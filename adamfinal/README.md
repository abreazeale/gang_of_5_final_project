# README File for Node Site Assigment
## Adam Breazeale
```console
The quick red fox jumps over the lazy brown dog.
```
## Assigment Link
+ 

I added this app (modified from /listUsers) to server.js
```js
app.get('/getMorality', function (req, res) {
    fs.readFile(__dirname + "/" + "nhs.json", 'utf8', function (err, data) {
        console.log(data);
       
        res.end(data);
    });
})
```

### These files are pulled from Rick's github:
+ chartjhs.html
+ server.js
+ user.json

