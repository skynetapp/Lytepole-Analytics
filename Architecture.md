#### Date: 17/03/2017

#### Description: This document explains the code flow of analytics graph.

#### The Folder Structure is as follows:

 Root Directory | Sub Directory 
------------ | -------------
index.php | 
Global | LytepoleWSConnection
Lib | Smarty,nusoap
Modules | Analytics
Views | AnalyticsJobdetail, AnalyticsForm4


#### Architecture

- After login into lytepole, on the side menu we can see the option **Analytics** where we can view the posted jobs and shared jobs in a graph for week, month and year.
- First it will get the user id and will get the jobs data into chart.
- To get post jobs by year function **getPostDataByYear** will be called.
- To get share jobs by year function **getPostDataByYear** will be called.
- To get post jobs by days function **getPostDataByYear** will be called. Days will be 7, 14, 30. 
- To get share jobs by days function **getPostDataByYear** will be called. Days will be 7, 14, 30.
- To view the shared and posted jobs graph form, **AnalyticsForm4.tpl** will be called which displays the graph accordingly.
- If we want to get the jobs between selected dates i.e cutome dates function **getCustomeChart** will be called.
- To view the Job detail of custome dates, function **showJobdetailViewAnalytics** will be called.
- To display the job graph form, tpl page will be as **AnalyticsJobdetail.tpl**.
