#### Step 1:

Function **getJobCustomeChart** will be called first from index.php to controller page which is used to get the jobs views of login user for custome dates.

- First it will get the user id by function **getUserID** from controller page and redirected to action page.
- In action page, first wsdl client connection will be set by function **setWSDLHandle** .
- From action page, Function **getUserID** will be redirected to AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Returns the login id as result to controller page.

#### Step 2:

 - Function **getApplicantsDataByCustome** from controller page and redirected to action page which is used to call the applicant views count by custome dates.
- Parameters will be job id, start date and end date.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getApplicantsDataByCustome** will be redirected to AnalyticsJobWS.php which is used to send data to DB to get applicants views by custome dates .
- Getting the mysql DB connection and calling the query from DB.
- Result returns the applicant views count to controller page.

#### Step 3:

 - Function **getViewsDataByCustome** from controller page and redirected to action page whichis used to call the views count by custome dates.
 - Parameters will be user id, start date and end date.
 - In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getViewsDataByCustome** will be redirected to AnalyticsJobWS.php which is used to send data to DB to get views by custome dates .
- Getting the mysql DB connection and calling the query from DB.
- Result returns the views count to controller page.
