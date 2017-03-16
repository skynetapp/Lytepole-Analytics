This Analytics module used to show the user settings..

#### Step 1:

Function **controlAnalyticsViewFlow** will be called first from index.php to controller which is used to get the jobs shared and posted of login user for week,month,year.

- First it will get the user id by function **getUserID**.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getUserID** in AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
