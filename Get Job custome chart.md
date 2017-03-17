#### Step 1:

Function **getJobCustomeChart** will be called first from index.php to controller is used to get the jobs views of login user for custome dates.

- First it will get the user id by function **getUserID**.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getUserID** in AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Result will be returned to controller.

#### Step 2:

 - Function **getApplicantsDataByCustome** is used to call the applicant views count by custome dates.
 - In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getApplicantsDataByCustome** is used to send data to DB to get applicants views by custome dates .
- Getting the mysql DB connection and calling the query from DB.
- Result returns the applicant views count to controller.

#### Step 3:

 - Function **getViewsDataByCustome** is used to call the views count by custome dates.
 - In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getViewsDataByCustome** is used to send data to DB to get views by custome dates .
- Getting the mysql DB connection and calling the query from DB.
- Result returns the views count to controller.
