# applenti_sealReport

#FrontEnd
1. Use the html to view reports in iframe
2. Currently "Users" and "Incidents" reports are already deployed to https://applenti-sealreports-dev.azurewebsites.net/ - could be changed to your service
3. Open the page in browser
4. Each button on click executes and fetches reports
5. Multiple options are provided for filtering and aggregation 
6. Export csv option should be available to download report


#Integration note
1. Authentication is not used and hence it is important to set few configuration parameters after deployment to be able to fetch reports in iframe
2. Access deployed service folder /site/wwwroot, and update the file web.config to following in <system.web> configuration
    <httpCookies httpOnlyCookies="false" requireSSL="true" sameSite="None"/>
    <sessionState cookieless="false" cookieSameSite="None" timeout="120" />
    
