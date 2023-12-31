# openapi_client.ClassLevelsApi

All URIs are relative to *https://www.dnd5eapi.co*

Method | HTTP request | Description
------------- | ------------- | -------------
[**api_classes_index_levels_class_level_features_get**](ClassLevelsApi.md#api_classes_index_levels_class_level_features_get) | **GET** /api/classes/{index}/levels/{class_level}/features | Get features available to a class at the requested level.
[**api_classes_index_levels_class_level_get**](ClassLevelsApi.md#api_classes_index_levels_class_level_get) | **GET** /api/classes/{index}/levels/{class_level} | Get level resource for a class and level.
[**api_classes_index_levels_get**](ClassLevelsApi.md#api_classes_index_levels_get) | **GET** /api/classes/{index}/levels | Get all level resources for a class.
[**api_classes_index_levels_spell_level_spells_get**](ClassLevelsApi.md#api_classes_index_levels_spell_level_spells_get) | **GET** /api/classes/{index}/levels/{spell_level}/spells | Get spells of the requested level available to the class.


# **api_classes_index_levels_class_level_features_get**
> APIReferenceList api_classes_index_levels_class_level_features_get(index, class_level)

Get features available to a class at the requested level.

### Example

```python
import time
import os
import openapi_client
from openapi_client.models.api_reference_list import APIReferenceList
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://www.dnd5eapi.co
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://www.dnd5eapi.co"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ClassLevelsApi(api_client)
    index = 'paladin' # str | The `index` of the class to get. 
    class_level = 3 # float | 

    try:
        # Get features available to a class at the requested level.
        api_response = api_instance.api_classes_index_levels_class_level_features_get(index, class_level)
        print("The response of ClassLevelsApi->api_classes_index_levels_class_level_features_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClassLevelsApi->api_classes_index_levels_class_level_features_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **index** | **str**| The &#x60;index&#x60; of the class to get.  | 
 **class_level** | **float**|  | 

### Return type

[**APIReferenceList**](APIReferenceList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_classes_index_levels_class_level_get**
> ClassLevel api_classes_index_levels_class_level_get(index, class_level)

Get level resource for a class and level.

### Example

```python
import time
import os
import openapi_client
from openapi_client.models.class_level import ClassLevel
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://www.dnd5eapi.co
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://www.dnd5eapi.co"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ClassLevelsApi(api_client)
    index = 'paladin' # str | The `index` of the class to get. 
    class_level = 3 # float | 

    try:
        # Get level resource for a class and level.
        api_response = api_instance.api_classes_index_levels_class_level_get(index, class_level)
        print("The response of ClassLevelsApi->api_classes_index_levels_class_level_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClassLevelsApi->api_classes_index_levels_class_level_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **index** | **str**| The &#x60;index&#x60; of the class to get.  | 
 **class_level** | **float**|  | 

### Return type

[**ClassLevel**](ClassLevel.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_classes_index_levels_get**
> List[ClassLevel] api_classes_index_levels_get(index, subclass=subclass)

Get all level resources for a class.

### Example

```python
import time
import os
import openapi_client
from openapi_client.models.class_level import ClassLevel
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://www.dnd5eapi.co
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://www.dnd5eapi.co"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ClassLevelsApi(api_client)
    index = 'paladin' # str | The `index` of the class to get. 
    subclass = 'berserker' # str | Adds subclasses for class to the response (optional)

    try:
        # Get all level resources for a class.
        api_response = api_instance.api_classes_index_levels_get(index, subclass=subclass)
        print("The response of ClassLevelsApi->api_classes_index_levels_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClassLevelsApi->api_classes_index_levels_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **index** | **str**| The &#x60;index&#x60; of the class to get.  | 
 **subclass** | **str**| Adds subclasses for class to the response | [optional] 

### Return type

[**List[ClassLevel]**](ClassLevel.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **api_classes_index_levels_spell_level_spells_get**
> APIReferenceList api_classes_index_levels_spell_level_spells_get(index, spell_level)

Get spells of the requested level available to the class.

### Example

```python
import time
import os
import openapi_client
from openapi_client.models.api_reference_list import APIReferenceList
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://www.dnd5eapi.co
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "https://www.dnd5eapi.co"
)


# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.ClassLevelsApi(api_client)
    index = 'paladin' # str | The `index` of the class to get. 
    spell_level = 4 # float | 

    try:
        # Get spells of the requested level available to the class.
        api_response = api_instance.api_classes_index_levels_spell_level_spells_get(index, spell_level)
        print("The response of ClassLevelsApi->api_classes_index_levels_spell_level_spells_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ClassLevelsApi->api_classes_index_levels_spell_level_spells_get: %s\n" % e)
```



### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **index** | **str**| The &#x60;index&#x60; of the class to get.  | 
 **spell_level** | **float**|  | 

### Return type

[**APIReferenceList**](APIReferenceList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

