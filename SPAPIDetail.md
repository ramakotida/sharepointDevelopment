1.# Validate user from sharepoint site url

https://<IP>/api/Pipflow/spcheckuser?uname=<spm>&pwd=<pip@123>
  
  Method type : GET or POST
  
  Request parameters:
             uname: user name
             pwd : password of the user
  Response output:
  
              success: true
              fail:  false
  
# end 

2.# Get the sharepont list details based on list name

https://<IP>/api/Pipflow/spgetListByName?Listname=<pipflow1>
  
  Method type : GET or POST
  
  Request parameters:
             Listname : Name of the list 
             
  Response output:
  
              success: "[{\"id\":\"37\",\"title\":\"testsdf\",\"status\":\"\",\"remarks\":\"\",\"taskoutcome\":null,\"Modified_By\":null,\"Modified_By_id\":null,\"Created_By\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"Created_By_id\":null,\"assigned_to\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"assigned_to_id\":null,\"Modified_Date\":\"Microsoft.SharePoint.Client.FieldUserValue\"}
              fail:  null
  
  eg url path : http://localhost:56643/api/Pipflow/spgetListByName?listname=pipflow1
# end 

2.# Get the sharepont list details based on list name

https://<IP>/api/Pipflow/spgetListByName?Listname=<pipflow1>
  
  Method type : GET or POST
  
  Request parameters:
             Listname : Name of the list 
             
  Response output:
  
              success: "[{\"id\":\"37\",\"title\":\"testsdf\",\"status\":\"\",\"remarks\":\"\",\"taskoutcome\":null,\"Modified_By\":null,\"Modified_By_id\":null,\"Created_By\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"Created_By_id\":null,\"assigned_to\":\"Microsoft.SharePoint.Client.FieldUserValue\",\"assigned_to_id\":null,\"Modified_Date\":\"Microsoft.SharePoint.Client.FieldUserValue\"}
              fail:  null
  
  eg url path : http://localhost:56643/api/Pipflow/spgetListByName?listname=pipflow1
# end 
