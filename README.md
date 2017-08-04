# Description
You want to use Arrow to track who likes your posts on Facebook

## API Management Version Compatibilty
This artefact was successfully tested for the following versions:
- Arrow 1.8.6


## Install
- First of all, open a Facebook Developer Account
https://developers.facebook.com/

- Then, create an application
  * https://developers.facebook.com/apps/
  * Write down the appId and appSecret
  * Make sure the “App Domains” and “Site URL” both includes “localhost” (in the Settings tab)

![alt text][Screenshot1] 

[Screenshot1]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot1.png  "Screenshot1"


- Facebook Setup – Create Sample Data
To test our arrow connector, we will need some sample data :
  * Two facebook pages : https://www.facebook.com/pages/create/
  * In each page, several posts
  * Several end-user accounts to actually like those posts

![alt text][Screenshot2] 

[Screenshot2]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot2.png  "Screenshot2" 


- Arrow Connector – Installation
First, clone the Github repository

- Arrow Connector – Publishing
The Arrow Connector for the Facebook Graph API must be publish by yourself in your private Arrow Connector repository

![alt text][Screenshot3] 

[Screenshot3]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot3.png  "Screenshot3" 


- Arrow Connector – Project Creation   
Create an Arrow project and then install the freshly published connector :

![alt text][Screenshot4] 

[Screenshot4]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot4.png  "Screenshot4" 


- Facebook – Get an Access Token
  * Go the the GitHub project downloaded before
  * Run the “get-oauth-token.sh” and pass your appId/appSecret as parameters
  * Write down the Access Token

![alt text][Screenshot5] 

[Screenshot5]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot5.png  "Screenshot5" 


  * Note, that you may have to approve the requested scopes:
  
![alt text][Screenshot6] 

[Screenshot6]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot6.png  "Screenshot6" 

  
- Arrow Connector – Edit configuration
  * Edit the “appc.facebook.default.js” and set the access token you received from Facebook 
  * Set to ”true” the “modelAutogen” and ”generateModelsFromSchema” properties

![alt text][Screenshot7] 

[Screenshot7]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot7.png  "Screenshot7" 


- Arrow Connector – Start the Arrow project
  * Start the Arrow Project (appc run -l debug) 
  * If your config is OK, you should get a success message in the output

![alt text][Screenshot8] 

[Screenshot8]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot8.png  "Screenshot8" 


## Usage
- Arrow Connector – Find the data in Facebook

![alt text][Screenshot9] 

[Screenshot9]: https://github.com/Axway-API-Management/Arrow-connector-using-facebook-GraphAPI/blob/master/Readme/Screenshot9.png  "Screenshot9" 


- Done so far…
  * Model generation 
  * Schema discovery
  * Read operations (query)


## Bug and Caveats
  * Clean up
  * Access_token renewal. Currently you have to update the Arrow configuration every 60 days with an updated access_token
  * Maybe split “posts” and “likes” in different models
  * See if the write operations are possible (Facebook GraphAPI is very restricted)

## Contributing

Please read [Contributing.md](https://github.com/Axway-API-Management/Common/blob/master/Contributing.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Team

![alt text][Axwaylogo] Axway Team

[Axwaylogo]: https://github.com/Axway-API-Management/Common/blob/master/img/AxwayLogoSmall.png  "Axway logo"


## License
[Apache License 2.0](/LICENSE))

