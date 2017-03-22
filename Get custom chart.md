#### Step 1:

Function **getCustomeChart** will be called first from index.php to controller page which is used to get the jobs shared and posted of login user for custome dates.

- First it will get the user id by function **getUserID** from controller page and redirected to action page.
- In action page, first wsdl client connection will be set by function **setWSDLHandle** .
- From action page, Function **getUserID** will be redirected to AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Returns the login id as result to controller page.

#### Step 2:

- Function **getPostDataByCustome** from controller page and redirected to action page which is used to call the posted jobs by custome dates.
- Input parameters will be user id, start date and end date.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getPostDataByCustome** will be redirected to AnalyticsWS.php which is used to send data to DB for get posted jobs by custome dates.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the posted jobs count to controller.

#### Step 3:

- Function **getShareDataByCustome** from controller page and redirected to action page which is used to call the shared jobs by custome dates.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getShareDataByCustome** will be redirected to AnalyticsWS.php which is used to send data to DB for get shared jobs by custome dates.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the shared jobs count to controller.

