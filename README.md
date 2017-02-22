# flash-comments
Flash Comments - Realtime Live Commenting using Pusher &amp; Websockets

## Prerequisite Softwares
- NodeJS
- NPM
- Yarn (Optional)

## Running the Project
In order to run the app on your machines, please follow the below given steps:

1. Clone the Repo using the URL - https://github.com/mappmechanic/flash-comments

```
 git clone https://github.com/mappmechanic/flash-comments.git
```

2. Run either of the following commands to install dependencies

```
 npm install
```

OR 

```
 yarn
```

3. Signup at [https://pusher.com/signup](https://pusher.com/signup).

4. Create a new app to obtain the API Key, secret & appId. Also, I have chosen the cluster **'ap2 (Mumbai, India)**, but you will be required to choose a cluster specific to your app users.

Replace the respective key, secret & appId for pusher initialisation in **server.js** file with your values:

```javascript
    var pusher = new Pusher({
    appId: '<your-app-id>',
    key: '<your-api-key>',
    secret: '<your-app-secret>',
    cluster: 'ap2',
    encrypted: true
    });
```

5. Finally you will have to also replace your app-key in **app.js** file too:

```javascript
 ...
 pusher = new Pusher('<your-api-key>', {
    cluster: 'ap2',
    encrypted: true
 }),
 ...
```

6. Now we are ready to run our app using the following node commands

```
node server
```

7. We will be able to access the app at [http://localhost:9000](http://localhost:9000)

For Any clarifications or questions Tweet to me at 
[https://twitter.com/mappmechanic](https://twitter.com/mappmechanic)



