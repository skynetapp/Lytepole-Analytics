#### Step 1:

Function **controlAnalyticsJobViewFlow** will be called first from index.php to controller is used to get the jobs views of login user for year,month,week.

- First it will get the user id by function **getUserID** from controller page and redirected to action page.
- In action page, first wsdl client connection will be set by function **setWSDLHandle** .
- From action page, Function **getUserID** will be redirected to AnalyticsWS.php will pass the session id to wsdl call **get_entry_list**.
- Returns the login id as result to controller page.
#### Step 2:

- Function **getApplicantsDataByYear** from controller page and redirected to action page which is used to call the applicants count by year.
- Input parameters will be Job id.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getApplicantsDataByYear** will be redirected to AnalyticsJobWS.php is used to send data to DB to get applicants views by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the applicant views count to controller.

#### Step 3:

- Function **getEmailViewsByYear** from controller page and redirected to action page which is used to call the email views count by year.
- Input parameters will be Job id.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getEmailViewsByYear** will be redirected to AnalyticsEmailWS.php is used to send data to DB for getting email views by year.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the email views count to controller.

#### Step 4:

- Function **getApplicantsDataBydays** from controller page and redirected to action page which is used to call the applicant views count by days.
- Input parameters will be Job id.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getApplicantsDataBydays**  will be redirected to AnalyticsJobWS.php is used to send data to DB to get applicants views by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the applicant views count to controller.
- It retrieves the applicant views count for 7, 14, 30 days.

#### Step 5:

- Function **getViewsDataBydays** from controller page and redirected to action page which is used to call the views count by days.
- Input parameters will be Job id.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getViewsDataBydays** will be redirected to AnalyticsJobWS.php is used to send data to DB to get views by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the views count to controller.
- It retrieves the views count for 7, 14, 30 days.

#### Step 6:

- Function **getEmailViewsBydays** from controller page and redirected to action page which is used to call the email views count by days.
- Input parameters will be Job id.
- In action page, first wsdl client connection will be set by function **setWSDLHandle**.
- From action page, Function **getEmailViewsBydays** will be redirected to AnalyticsJobWS.php is used to send data to DB to get email views by days.
- Getting the mysql DB connection and calling the query from DB.
- Result returns the email views count to controller.
- It retrieves the email views count for 7, 14, 30 days.

#### Step 7:

- Function **showJobdetailViewAnalytics** is used to show the views job graph form.
- The parameters passed are applicant data, view data, email views, job id.
- From action page, function **showJobdetailViewAnalytics** will be redirected to AnalyticsView.php to display the tpl page.
- The display tpl page will be **AnalyticsJobdetail.tpl** which will be in views folder.

