#### Step 1:

Function **getCustomeChart** will be called first from index.php to controller is used to get the jobs shared and posted of login user for custome dates.

- First it will get the user id by function **getUserID**.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getUserID** in AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Result will be returned to controller.

#### Step 2:

- Function **getPostDataByCustome** is used to call the posted jobs by custome dates.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getPostDataByCustome** is used to send data to DB for get posted jobs by custome dates.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the posted jobs count to controller.

#### Step 3:

- Function **getShareDataByCustome** is used to call the shared jobs by custome dates.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getShareDataByCustome** is used to send data to DB for get shared jobs by custome dates.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the shared jobs count to controller.

