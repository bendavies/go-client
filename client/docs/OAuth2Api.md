# \OAuth2Api

All URIs are relative to *https://api.moov.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CheckOAuthClientCredentials**](OAuth2Api.md#CheckOAuthClientCredentials) | **Get** /v1/oauth2/authorize | Verify OAuth2 Bearer token
[**CreateOAuth2Client**](OAuth2Api.md#CreateOAuth2Client) | **Post** /v1/oauth2/client | Create OAuth2 client credentials
[**CreateOAuth2Token**](OAuth2Api.md#CreateOAuth2Token) | **Post** /v1/oauth2/token | Generate OAuth2 access token


# **CheckOAuthClientCredentials**
> CheckOAuthClientCredentials(ctx, authorization)
Verify OAuth2 Bearer token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **authorization** | **string**| &lt;ignored&gt; | 

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateOAuth2Client**
> OAuth2Clients CreateOAuth2Client(ctx, )
Create OAuth2 client credentials

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**OAuth2Clients**](OAuth2Clients.md)

### Authorization

[cookieAuth](../README.md#cookieAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateOAuth2Token**
> map[string]interface{} CreateOAuth2Token(ctx, optional)
Generate OAuth2 access token

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***CreateOAuth2TokenOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a CreateOAuth2TokenOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **grantType** | **optional.String**| OAuth2 grant type (must be &#39;client_credentials&#39;) | [default to client_credentials]
 **clientId** | **optional.String**| OAuth2 client ID | 
 **clientSecret** | **optional.String**| OAuth2 client secret | 

### Return type

[**map[string]interface{}**](map[string]interface{}.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)
