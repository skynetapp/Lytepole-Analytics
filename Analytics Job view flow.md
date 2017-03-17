#### Step 1:

Function **controlAnalyticsJobViewFlow** will be called first from index.php to controller is used to get the jobs views of login user for year,month,week.

- First it will get the user id by function **getUserID**.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getUserID** in AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Result will be returned to controller.

#### Step 2:

- Function **getApplicantsDataByYear** is used to call the applicants count by year.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getApplicantsDataByYear** in AnalyticsJobWS.php is used to send data to DB to get applicants views by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the applicant views count to controller.

#### Step 3:

- Function **getEmailViewsByYear** is used to call the email views count by year.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getEmailViewsByYear** in AnalyticsEmailWS.php is used to send data to DB for getting email views by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the email views count to controller.

#### Step 4:

- Function **getApplicantsDataBydays** is used to call the applicant views count by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getApplicantsDataBydays** in AnalyticsJobWS.php is used to send data to DB to get applicants views by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the applicant views count to controller.
- It retrieves the applicant views count for 7, 14, 30 days.

#### Step 5:

- Function **getViewsDataBydays** is used to call the views count by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getViewsDataBydays** in AnalyticsJobWS.php is used to send data to DB to get views by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the views count to controller.
- It retrieves the views count for 7, 14, 30 days.

#### Step 6:

- Function **getEmailViewsBydays** is used to call the email views count by days.
- In action, first wsdl client connection will be set by function **setWSDLHandle**.
- Function **getEmailViewsBydays** in AnalyticsEmailWS.php is used to send data to DB to get email views by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the email views count to controller.
- It retrieves the email views count for 7, 14, 30 days.

#### Step 7:

- Function **showJobdetailViewAnalytics** is used to show the views job graph form.
- In action, function **showJobdetailViewAnalytics** will be called from AnalyticsView.php to display the tpl page.
- The display tpl page will be **AnalyticsJobdetail.tpl** which will be in views folder.

