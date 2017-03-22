This Analytics module used to show the user settings..

#### Step 1:

Function **controlAnalyticsViewFlow** will be called first from index.php to controller page which is used to get the jobs shared and posted of login user for week,month,year.

- First it will get the user id by function **getUserID** from controller page and redirected to action page.
- In action page, first wsdl client connection will be set by function **setWSDLHandle** .
- From action page, Function **getUserID** will be redirected to AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Returns the login id as result to controller page.

#### Step 2:

- Function **getPostDataByYear** from controller page and redirected to action page which is used to call the posted jobs by year.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getPostDataByYear** will be redirected to AnalyticsWS.php which is used to send data to DB for get posted jobs by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the posted jobs count to controller page.

#### Step 3:

- Function **getShareDataByYear** from controller page and redirected to action page which is used to call the shared jobs by year.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getShareDataByYear** will be redirected to AnalyticsWS.php which is used send data to DB for get shared jobs by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the shared jobs count to controller.

#### Step 4:

- Function **getPostDataBydays** from controller page and redirected to action page which is used to call the posted jobs by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getPostDataBydays** will be redirected to AnalyticsWS.php which is used send data to DB for get posted jobs by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the posted jobs count to controller.
- It retrieves the jobs count for 7, 14, 30 days.

#### Step 5:

- Function **getShareDataBydays** from controller page and redirected to action page which is used to call the shared jobs by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getShareDataBydays** will be redirected to AnalyticsWS.php which is used send data to DB for get shared jobs by custome dates.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the shared jobs count to controller.
- It retrieves the jobs count for 7, 14, 30 days.

#### Step 6:

- Function **showYeardataView** from controller page and redirected to action page which is used to show the shared and posted job graph form.
- From action page, function **showYeardataView** will be redirected to AnalyticsView.php to display the tpl page.
- The display tpl page will be **AnalyticsForm4.tpl** which will be in views folder.





