# DefaultApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AddNextflowEventNextflowEventsPost**](DefaultApi.md#AddNextflowEventNextflowEventsPost) | **POST** /nextflow/events | Add Nextflow Event
[**AddUserUsersPost**](DefaultApi.md#AddUserUsersPost) | **POST** /users | Add User
[**DeleteUserUsersUidDelete**](DefaultApi.md#DeleteUserUsersUidDelete) | **DELETE** /users/{uid} | Delete User
[**FilesChangeFilesChangesPost**](DefaultApi.md#FilesChangeFilesChangesPost) | **POST** /files/changes | Files Change
[**GenerateDownloadSignedUrlV4FilesSignedGet**](DefaultApi.md#GenerateDownloadSignedUrlV4FilesSignedGet) | **GET** /files/signed | Generate Download Signed Url V4
[**GetNextflowEventNextflowEventsIdGet**](DefaultApi.md#GetNextflowEventNextflowEventsIdGet) | **GET** /nextflow/events/{id} | Get Nextflow Event
[**GetUserUsersUidGet**](DefaultApi.md#GetUserUsersUidGet) | **GET** /users/{uid} | Get User
[**ListFileEventsFilesChangesGet**](DefaultApi.md#ListFileEventsFilesChangesGet) | **GET** /files/changes | List File Events
[**ListNextflowEventsNextflowEventsGet**](DefaultApi.md#ListNextflowEventsNextflowEventsGet) | **GET** /nextflow/events | List Nextflow Events
[**ListUsersUsersGet**](DefaultApi.md#ListUsersUsersGet) | **GET** /users | List Users


# **AddNextflowEventNextflowEventsPost**
> AnyType AddNextflowEventNextflowEventsPost(nextflow.event.model)

Add Nextflow Event

Events from running Nextflow pipelines when using -with-weblog.  See [the Nextflow documentation](https://www.nextflow.io/docs/latest/tracing.html#weblog-via-http).

### Example
```R
library(metagenomicsClientR)

var.nextflow.event.model <- NextflowEventModel$new("runName_example", "runId_example", "event_example", "utcTime_example", 123, 123) # NextflowEventModel | 

#Add Nextflow Event
api.instance <- DefaultApi$new()
result <- api.instance$AddNextflowEventNextflowEventsPost(var.nextflow.event.model)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **nextflow.event.model** | [**NextflowEventModel**](NextflowEventModel.md)|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **AddUserUsersPost**
> AnyType AddUserUsersPost(user.model)

Add User

### Example
```R
library(metagenomicsClientR)

var.user.model <- UserModel$new("name_example") # UserModel | 

#Add User
api.instance <- DefaultApi$new()
result <- api.instance$AddUserUsersPost(var.user.model)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user.model** | [**UserModel**](UserModel.md)|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **DeleteUserUsersUidDelete**
> AnyType DeleteUserUsersUidDelete(uid)

Delete User

### Example
```R
library(metagenomicsClientR)

var.uid <- 56 # integer | 

#Delete User
api.instance <- DefaultApi$new()
result <- api.instance$DeleteUserUsersUidDelete(var.uid)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uid** | **integer**|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **FilesChangeFilesChangesPost**
> AnyType FilesChangeFilesChangesPost(body)

Files Change

Track all changes in cloud storage

### Example
```R
library(metagenomicsClientR)

var.body <- NULL # object | 

#Files Change
api.instance <- DefaultApi$new()
result <- api.instance$FilesChangeFilesChangesPost(var.body)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **GenerateDownloadSignedUrlV4FilesSignedGet**
> AnyType GenerateDownloadSignedUrlV4FilesSignedGet(name)

Generate Download Signed Url V4

Generates a v4 signed URL for downloading a blob.  Note that this method requires a service account key file. You can not use this if you are using Application Default Credentials from Google Compute Engine or from the Google Cloud SDK.

### Example
```R
library(metagenomicsClientR)

var.name <- 'name_example' # character | 

#Generate Download Signed Url V4
api.instance <- DefaultApi$new()
result <- api.instance$GenerateDownloadSignedUrlV4FilesSignedGet(var.name)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **character**|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **GetNextflowEventNextflowEventsIdGet**
> AnyType GetNextflowEventNextflowEventsIdGet(id)

Get Nextflow Event

### Example
```R
library(metagenomicsClientR)

var.id <- 'id_example' # character | 

#Get Nextflow Event
api.instance <- DefaultApi$new()
result <- api.instance$GetNextflowEventNextflowEventsIdGet(var.id)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | [**character**](.md)|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **GetUserUsersUidGet**
> AnyType GetUserUsersUidGet(uid)

Get User

### Example
```R
library(metagenomicsClientR)

var.uid <- 56 # integer | 

#Get User
api.instance <- DefaultApi$new()
result <- api.instance$GetUserUsersUidGet(var.uid)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **uid** | **integer**|  | 

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **ListFileEventsFilesChangesGet**
> StorageEventCollection ListFileEventsFilesChangesGet(limit=100, offset=0, start.date=var.start.date, end.date=var.end.date, filename.regex=var.filename.regex)

List File Events

### Example
```R
library(metagenomicsClientR)

var.limit <- 100 # integer | 
var.offset <- 0 # integer | 
var.start.date <- 'start.date_example' # character | 
var.end.date <- 'end.date_example' # character | 
var.filename.regex <- 'filename.regex_example' # character | 

#List File Events
api.instance <- DefaultApi$new()
result <- api.instance$ListFileEventsFilesChangesGet(limit=var.limit, offset=var.offset, start.date=var.start.date, end.date=var.end.date, filename.regex=var.filename.regex)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **integer**|  | [optional] [default to 100]
 **offset** | **integer**|  | [optional] [default to 0]
 **start.date** | **character**|  | [optional] 
 **end.date** | **character**|  | [optional] 
 **filename.regex** | **character**|  | [optional] 

### Return type

[**StorageEventCollection**](StorageEventCollection.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **ListNextflowEventsNextflowEventsGet**
> AnyType ListNextflowEventsNextflowEventsGet(limit=100, offset=0)

List Nextflow Events

### Example
```R
library(metagenomicsClientR)

var.limit <- 100 # integer | 
var.offset <- 0 # integer | 

#List Nextflow Events
api.instance <- DefaultApi$new()
result <- api.instance$ListNextflowEventsNextflowEventsGet(limit=var.limit, offset=var.offset)
dput(result)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **integer**|  | [optional] [default to 100]
 **offset** | **integer**|  | [optional] [default to 0]

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

# **ListUsersUsersGet**
> AnyType ListUsersUsersGet()

List Users

### Example
```R
library(metagenomicsClientR)


#List Users
api.instance <- DefaultApi$new()
result <- api.instance$ListUsersUsersGet()
dput(result)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AnyType**](AnyType.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

