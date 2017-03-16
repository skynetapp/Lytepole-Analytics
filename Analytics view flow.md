This Analytics module used to show the user settings..

#### Step 1:

Function **controlAnalyticsViewFlow** will be called first from index.php to controller which is used to get the jobs shared and posted of login user for week,month,year.

- First it will get the user id by function **getUserID**.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getUserID** in AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Result will be returned to controller.

#### Step 2:

- Function **getPostDataByYear** is used to call the posted jobs by year.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getPostDataByYear** is used to send data to DB for get posted jobs by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the posted jobs count to controller.

#### Step 3:

- Function **getShareDataByYear** is used to call the shared jobs by year.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getShareDataByYear** is used send data to DB for get shared jobs by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the shared jobs count to controller.

#### Step 4:

- Function **getPostDataBydays** is used to call the posted jobs by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getPostDataBydays** is used send data to DB for get posted jobs by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the posted jobs count to controller.
- It retrieves the jobs count for 7, 14, 30 days.

#### Step 5:

- Function **getShareDataBydays** is used to call the shared jobs by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getShareDataBydays** is used send data to DB for get shared jobs by custome dates.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the shared jobs count to controller.
- It retrieves the jobs count for 7, 14, 30 days.

#### Step 6:

- Function **showYeardataView** is used to show the shared and posted job graph form.
- In action, function **showYeardataView** will be called from AnalyticsView.php to display the tpl page.
- The display tpl page will be **AnalyticsForm4.tpl** which will be in views folder.





