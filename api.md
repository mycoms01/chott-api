#001
get {{BaseUrl}}/api/v1/lineoa/master/location
    body:{
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":[
            {
            "locationId": "UUID",
            "locationNameDisplay": "string",
            "locationName": "string",
            }
        ]
            
    }

#002
post {{BaseUrl}}/api/v1/lineoa/master/user
    body:{
        "projectCode":"string",
        "locationId":"uuid",
        "customerName":"string",
        "phoneNumber":"string",
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":{
            "id":"UUID"
            }
            
    }
#003
put {{BaseUrl}}/api/v1/lineoa/master/user/:id
    body:{
        "projectCode":"string",
        "locationId":"uuid",
        "customerName":"string"
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":{
            "id":"UUID"
            }
            
    }

#004    
get {{BaseUrl}}/api/v1/lineoa/master/user?projectCode=&searchName=&searchLocation=
    body:{}
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":[
            {
             "id":"UUID",
             "locationId":"uuid",
             "locationName":"string",
             "customerName":"string",
             "phoneNumber":"string",
             "registerDateTime":"string",
            }
            ]
            
    }
#005
get {{BaseUrl}}/api/v1/lineoa/master/user/:id
    body:{}
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
             "locationId":"uuid",
             "locationName":"string",
             "customerName":"string",
             "phoneNumber":"string",
             "registerDateTime":"string",
            }
    }
#006
del {{BaseUrl}}/api/v1/lineoa/master/user/:id
    body:{}
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
            }
    }

#007
post {{BaseUrl}}/api/v1/lineoa/service/otp
    body:{}
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
            }
    }

#008
post {{BaseUrl}}/api/v1//lineoa/service/user/:id/request
    body:{
        serviceAccessTypeCode:int,
         locationId:"",
        requests:[
            {
                details:"",
                date:"",
                hourStart:"",
                hourEnd:"",
                limit:1
                images:[]
            },
            {
                details:"",
                date:"",
               hourStart:"",
                hourEnd:"",
                limit:1
                images:[]
            }
        ]
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            [
            {
             "id":"UUID",
            },
            {
             "id":"UUID",
            }
            ]
    }

#009   
get {{BaseUrl}}/api/v1/lineoa/service/user/:id/request/
    body:{}
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":[
            {
             "id":"UUID",
             "projectCode":"string",
             "projectName":"string",
             "taskCode":"string",
             "createDateTime":"string",
             "slotId":"string",
             "slotName":"string",
             "details":"string",
             "locationId":"uuid",
             "locationName":"string",
             "customerName":"string",
             "phoneNumber":"string",
             "registerDateTime":"string",
             "serviceAccessTypeCode":"int",
             "serviceAccessTypeName":"string"
            }
            ]
            
    }
#010   
get {{BaseUrl}}/api/v1/lineoa/service/user/:id/request/:id
    body:{}
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
             "projectCode":"string",
             "projectName":"string",
             "taskCode":"string",
             "createDateTime":"string",
             "slotId":"UUID",
             "slotName":"string",
             "details":"string",
             "locationId":"uuid",
             "locationName":"string",
             "customerName":"string",
             "phoneNumber":"string",
             "registerDateTime":"string",
             "serviceAccessTypeCode":"int",
             "serviceAccessTypeName":"string"
             "image":{
                "id":"",
                "url":""
             }
            }
            
            
    }
#011  
put {{BaseUrl}}/api/v1/lineoa/service/user/:id/request/:id
    body:{
        "date":"date",
        "slot":"int",
        "serviceAccessTypeCode":"int",
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
            }
    }
#012  
post {{BaseUrl}}/api/v1/lineoa/service/user/:id/complaint
    body:{
        "complaintTypeCode":"int",
        "desc":"string",
        "image":"UUID"
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
            }
    }
#013  
get {{BaseUrl}}/api/v1/lineoa/service/complaint?projectCode=&searchName=&searchLocation=&complaintTypeCode=&statusCode=&searchCode&complaintCode=
    body:{

    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":{},
        "data":[
            {
              "id":"UUID",
              "complaintCode":"string",
              "desc":"",
              "locationId":"uuid",
              "locationName":"string",
              "customerName":"string",
              "phoneNumber":"string",
              "complaintDateTime":"string",
              "complaintTypeCode":"int",
              "complaintTypeName":"string",
              "statusCode":"int",
            }
        ]
    }
#014  
get {{BaseUrl}}/api/v1/lineoa/service/complaint/:id
    body:{

    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":{},
        "data":
            {
              "id":"UUID",
              "complaintCode":"string",
              "desc":"",
              "locationId":"uuid",
              "locationName":"string",
              "customerName":"string",
              "phoneNumber":"string",
              "complaintDateTime":"string",
              "complaintTypeCode":"int",
              "complaintTypeName":"string",
              "statusCode":"int",
              "solution": "string",
`             "causes": "string",
              "preventionMethods" : "string",
              "imageBefore":"",
              "imageAfter":""
            }
        
    }
    
#015  
put {{BaseUrl}}/api/v1/lineoa/service/complaint/:id
    body:{
         "projectCode":"SPY"
        "solution": "string",
        "causes": "string",
        "preventionMethods" : "string",
        "imageBefore":null,
        "imageAfter":null
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":{},
        "data":
            {
              "id":"UUID",
            }
        
    }
    
#016  
post {{BaseUrl}}/api/v1/lineoa/service/upload?projectCode=
    body:{
        "files":"file",  
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":null,
        "data":
            {
              "id":"UUID",
            }
        
    }
#017
post {{BaseUrl}}/api/v1/lineoa/service/verifyotp
    body:{
         "projectCode":"string",
         "phoneNumber":"string",
         "transactionId":"uuid",
         "otpCode":"string",
         "refCode":"string",
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
             "id":"UUID",
            }
    }

    #018

get {{BaseUrl}}/api/v1/lineoa/master/slot?date=&projectCode=
    body:{
        
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":
            {
            "hourStart":"string",
            "hourEnd":"string",
            "hour":"string",
            "limit":"string",
            "using":"string",
            "available":"string"
            }
    }
    #019

get {{BaseUrl}}/api/v1/lineoa/master/serviceaccesstype
    body:{
        
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":[
            {
            "serviceAccessTypeCode":"int",
            "serviceAccessTypeName":"string",
            }
        ]
    }

   #020

del {{BaseUrl}}/api/v1/lineoa/service/user/:id/request/:id/cancel
    body:{
        
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":[
            {
            "id":"UUID",
           
            }
        ]
    }
       #021

get {{BaseUrl}}/api/v1/lineoa/service/complaint/summary
    body:{
        
    }
    response:{
        "status":{
            "statusCode": 200,
            "statusText": "Ok",
            "message": "โอเค" 
        },
        "pagination":NULL,
        "data":[
            {
            "statusCode":"int",
            "statusName":"string",
            "total":"int",
            }
        ]
    }