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