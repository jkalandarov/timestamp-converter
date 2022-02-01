<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        body { 
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;      
            color: #333;        
            background-color: #f6f6f6;    
        }
        .container {
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;    
        }
        li {
            margin-bottom: 10px;
        }
        li, p {
            font-size: 18px;
        }
        code {
            font-size: 90%;
        }
        a {
            color: #006fc6;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>API Project: Timestamp Microservice</h1>
        <h3>User Stories:</h1>
        <ol class="user-stories">
            <li>The API endpoint is <code>GET [project_url]/api/timestamp/:date_string</code></li>
            <li>A date string is valid if can be successfully parsed by <code>new Date(date_string)</code>.
                <br>
                Note that the unix timestamp needs to be an <strong>integer</strong> (not a string) specifying <strong>milliseconds</strong>.
                <br>
                In our test we will use date strings compliant with ISO-8601 (e.g. <code>"2016-11-20"</code>) because this will ensure an UTC timestamp.</li>
            <li>If the date string is <strong>empty</strong> it should be equivalent to trigger <code>new Date()</code>, i.e. the service uses the current timestamp.</li>
            <li>If the date string is <strong>valid</strong> the api returns a JSON having the structure
                <br>
                <code>{"unix": <date.getTime()>, "utc" : <date.toUTCString()> }</code
                ><br>
                e.g. <code>{"unix": 1479663089000 ,"utc": "Sun, 20 Nov 2016 17:31:29 GMT"}</code></li>
            <li>If the date string is <strong>invalid</strong> the api returns a JSON having the structure 
                <br>
                <code>{"error" : "Invalid Date" }</code>.
            </li>
        </ol>

        <h3>Example Usage:</h3>
        <ul>
            <li><a href="api/timestamp/2015-12-25">[project url]/api/timestamp/2015-12-25</a></li>
            <li><a href="api/timestamp/1450137600000">[project url]/api/timestamp/1450137600</a></li>
        </ul>

        <h3>Example Output:</h3>
        <p><code>{"unix":1451001600000, "utc":"Fri, 25 Dec 2015 00:00:00 GMT"}</code></p>
    </div>
</body>
</html>