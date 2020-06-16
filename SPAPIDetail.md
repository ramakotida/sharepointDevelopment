1.
# Validate user from sharepoint site url

https://<IP>/api/Pipflow/spcheckuser?uname=<spm>&pwd=<pip@123>
  
  Method type : GET or POST
  
  Request parameters:
             uname: user name
             pwd : password of the user
  Response output:
  
              success: true
              fail:  false
  
# end 

2.
# Get the sharepont list details based on list name

https://<IP>/api/Pipflow/spgetListByName?Listname=<pipflow1>
  
  Method type : GET or POST
  
  Request parameters:
             Listname : Name of the list 
             
  Response output:
  
              success: "[{\"id\":\"37\",\"title\":\"testsdf\",\"status\":\"\",\"remarks\":\"\",\"taskoutcome\":null,\"Modified_By\":null,\"Modified_By_id\":null,\"Created_By\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"Created_By_id\":null,\"assigned_to\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"assigned_to_id\":null,\"Modified_Date\":\"Microsoft.SharePoint.Client.FieldUserValue\"}
              fail:  null
  
  eg url path : http://localhost:56643/api/Pipflow/spgetListByName?listname=pipflow1
# end 

3.
# Set the sharepont list Item cretion based on TItle and remarks

https://<IP>/api/Pipflow/spsetFMR?fmrid=<fmrid>&remarks=<remarks>&Listname=<Listname>
  
  Method type : GET or POST
  
  Request parameters:
             fmrid : Send details of FMR      
             remarks : Send remarks
             Listname : Name of the list 
             
  Response output:
  
              success: success
              fail:  exception string will send
  
  eg url path : http://localhost:56643/api/Pipflow/spsetfmr?fmrid=1.1.1.3&remarks=testindf%20&listname=pipflow1
# end 
4.
# Get the sharepont list Item  based on TItle and remarks

https://<IP>api/Pipflow/spgetListItemByID?listname=<pipflow1>&ListitemId=<43>
  
  Method type : GET or POST
  
  Request parameters:
             Listname : Name of the list 
             ListitemId : LIst item id
             
  Response output:
  
              success: "[{\"id\":null,\"title\":\"1.1.1.1\",\"status\":\"inprogress\",\"remarks\":\"teswting rom data\",\"taskoutcome\":null,\"Modified_By\":null,\"Modified_By_id\":null,\"Created_By\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"Created_By_id\":null,\"assigned_to\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"assigned_to_id\":null,\"Modified_Date\":\"Microsoft.SharePoint.Client.FieldUserValue\"}]"
              fail:  exception string will send
  
  eg url path : http://localhost:56643/api/Pipflow/spgetListItemByID?listname=pipflow1&ListitemId=43
# end 
5.
# Get the sharepont list Item  based on TItle and remarks

https://<IP>api/Pipflow/spsetTaskItemByID?status=<Approved>&percentComplete=<1>&comments=<how%20r%20ou>&taskid=<449>&createdby=<spm>
  
  Method type : GET or POST
  
  Request parameters:
             status : Approved or Rejected or Assign to MD 
             percentComplete : 1 for 100%
             comments : user comments
             createdby : user login name
  Response output:
  
              success: "[{\"id\":null,\"title\":\"1.1.1.1\",\"status\":\"inprogress\",\"remarks\":\"teswting rom data\",\"taskoutcome\":null,\"Modified_By\":null,\"Modified_By_id\":null,\"Created_By\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"Created_By_id\":null,\"assigned_to\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"assigned_to_id\":null,\"Modified_Date\":\"Microsoft.SharePoint.Client.FieldUserValue\"}]"
              fail:  exception string will send
  
  eg url path : http://localhost:56643/api/Pipflow/spsetTaskItemByID?status=Approved&percentComplete=1&comments=how%20r%20ou&taskid=449&createdby=spm
# end 
6.
# Get the sharepont list Item  based on TItle and remarks

https://<IP>api/Pipflow/spgetTaskDetailsByuser?listname=<tasklist>&ListitemId=<449>
  
  Method type : GET or POST
  
  Request parameters:
             Listname : Name of the list 
             ListitemId : LIst item id
             
  Response output:
  
              success: "[{\"id\":null,\"title\":\"Task start and assing by i:0#.w|mylabsp\\\\spm\",\"status\":\"Approved\",\"remarks\":null,\"taskoutcome\":\"Approved\",\"Modified_By\":\"SPM\",\"Modified_By_id\":\"26\",\"Created_By\":\"SharePoint App\",\"Created_By_id\":\"1073741822\",\"assigned_to\":\"SPM\",\"assigned_to_id\":\"26\",\"Modified_Date\":null}]"
              fail:  exception string will send
  
  eg url path : http://localhost:56643/api/Pipflow/spgetTaskDetailsByuser?listname=tasklist&ListitemId=449
# end 
7.
# Get the sharepont list Item  based on TItle and remarks

http://<IP>api/Pipflow/spgetTaskDetails?listname=<tasklist>&Taskuser=<user name>
  
  Method type : GET or POST
  
  Request parameters:
             Listname : Name of the list 
             Taskuser : Pass user name
             
  Response output:
  
              success: "[{\"id\":\"1\",\"title\":\"new task assing by         System Account\",\"status\":\"Completed\",\"remarks\":null,\"taskoutcome\":\"Approved\",\"Modified_By\":\"System Account\",\"Modified_By_id\":\"1073741823\",\"Created_By\":\"SharePoint App\",\"Created_By_id\":\"1073741822\",\"assigned_to\":\"sp admin\",\"assigned_to_id\":\"1\",\"Modified_Date\":null},{\"id\":\"2\",\"title\":\"new task assing by         System Account\",\"status\":\"Not Started\",\"remarks\":null,\"taskoutcome\":\"\",\"Modified_By\":\"SharePoint App\",\"Modified_By_id\":\"1073741822\",\"Created_By\":\"SharePoint App\",\"Created_By_id\":\"1073741822\",\"assigned_to\":\"sp admin\",\"assigned_to_id\":\"1\",\"Modified_Date\":null},{\"id\":\"3\",\"title\":\"new task assing by         System Account\",\"status\":\"Not Started\",\"remarks\":null,\"taskoutcome\":\"\",\"Modified_By\":\"SharePoint App\",\"Modified_By_id\":\"1073741822\",\"Created_By\":\"SharePoint App\",\"Created_By_id\":\"1073741822\",\"assigned_to\":\"sp admin\",\"assigned_to_id\":\"1\",\"Modified_Date\":null},{\"id\":\"4\",\"title\":\"new task assing by         System Account\",\"status\":\"Completed\",\"remarks\":null,\"taskoutcome\":\"Reject to Assignee\",\"Modified_By\":\"System Account\",\"Modified_By_id\":\"1073741823\",\"Created_By\":\"SharePoint App\",\"Created_By_id\":\"1073741822\",\"assigned_to\":\"sp admin\",\"assigned_to_id\":\"1\",\"Modified_Date\":null},{\"id\":\"5\",\"title\":\"new task assing by         System Account\",\"status\":\"Not Started\",\"remarks\":null,\"taskoutcome\":\"\",\"Modified_By\":\"SharePoint App\",\"Modified_By_id\":\"1073741822\",\"Created_By\":\"SharePoint App\",\"Created_By_id\":\"1073741822\",\"assigned_to\":\"sp admin\",\"assigned_to_id\":\"1\",\"Modified_Date\":null}]"
              fail:  exception string will send
  
  eg url path : http://localhost:56643/api/Pipflow/spgetTaskDetails?listname=tasklist&Taskuser=sdfdf
# end 
