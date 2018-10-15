
## Build the Project
```
mvn clean install
```



## Projects/Modules
This project contains a number of modules, but here are the main ones you should focus on and run: 
- `oauth-authorization-server` - the Authorization Server (port = 8081)
- `oauth-resource-server-1` - the Resource Server (port = 8082)
- `oauth-resource-server-2` - the secondary Resource Server (port = 8088)


UI Modules: 
- `oauth-ui-implicit-angular4` - Implicit Grant UI Module - using Angular 4
- `oauth-ui-password-angular4` - Password Grant UI Module - using Angular 4
- `oauth-ui-authorization-code-angular` - Authorization code UI Module - using Angular 4


## Run the Modules
You can run any sub-module using command line: 
```
mvn spring-boot:run
```

If you're using Spring STS, you can also import them and run them directly, via the Boot Dashboard 

You can then access the UI application - for example the module using the Password Grant - like this: 
`http://localhost:8084/`

You can login using these credentials, username:john and password:123 

## Run the Angular 4 Modules

- To run any of Angular4 front-end modules (_spring-security-oauth-ui-implicit-angular4_ and _spring-security-oauth-ui-password-angular4_) , we need to build the app first:
```
mvn clean install
```

- Then we need to navigate to our Angular app directory:
```
cd src/main/resources
```

And run the command to download the dependencies:
```
npm install
```

- Finally, we will start our app:
```
npm start
```
- Note: Angular4 modules are commented out because these don't build on Jenkins as they need npm installed, but they build properly locally
- Note for Angular version < 4.3.0: You should comment out the HttpClient and HttpClientModule import in app.module and app.service.ts. These version rely on the HttpModule.
