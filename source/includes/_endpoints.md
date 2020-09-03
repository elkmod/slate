# /context

## readContext

> **Responses**



> 200 - Context

```json
{
    "token": "some-string",
    "currentCustomerGroup": {
        "name": "some-string",
        "displayGross": true
    },
    "fallbackCustomerGroup": {
        "name": "some-string",
        "displayGross": true
    },
    "currency": {
        "isoCode": "some-string",
        "factor": 42,
        "symbol": "some-string",
        "shortName": "some-string",
        "name": "some-string",
        "position": 42,
        "decimalPrecision": 42,
        "isSystemDefault": true
    },
    "salesChannel": {
        "typeId": "some-string",
        "languageId": "some-string",
        "currencyId": "some-string",
        "paymentMethodId": "some-string",
        "shippingMethodId": "some-string",
        "countryId": "some-string",
        "navigationCategoryId": "some-string",
        "navigationCategoryDepth": 42,
        "footerCategoryId": "some-string",
        "serviceCategoryId": "some-string",
        "name": "some-string",
        "shortName": "some-string",
        "accessKey": "some-string",
        "active": true,
        "maintenance": true,
        "maintenanceIpWhitelist": "some-string",
        "mailHeaderFooterId": "some-string",
        "customerGroupId": "some-string",
        "hreflangActive": true,
        "hreflangDefaultDomainId": "some-string",
        "analyticsId": "some-string"
    },
    "taxRules": [],
    "customer": {
        "groupId": "some-string",
        "defaultPaymentMethodId": "some-string",
        "salesChannelId": "some-string",
        "languageId": "some-string",
        "lastPaymentMethodId": "some-string",
        "defaultBillingAddressId": "some-string",
        "defaultShippingAddressId": "some-string",
        "customerNumber": "some-string",
        "salutationId": "some-string",
        "firstName": "some-string",
        "lastName": "some-string",
        "company": "some-string",
        "password": "some-string",
        "email": "some-string",
        "title": "some-string",
        "affiliateCode": "some-string",
        "campaignCode": "some-string",
        "active": true,
        "doubleOptInRegistration": true,
        "doubleOptInEmailSentDate": "some-string",
        "doubleOptInConfirmDate": "some-string",
        "hash": "some-string",
        "guest": true,
        "firstLogin": "some-string",
        "lastLogin": "some-string",
        "newsletter": true,
        "birthday": "some-string",
        "lastOrderDate": "some-string",
        "orderCount": 42,
        "legacyEncoder": "some-string",
        "legacyPassword": "some-string",
        "autoIncrement": 42,
        "remoteAddress": "some-string"
    },
    "paymentMethod": {
        "pluginId": "some-string",
        "handlerIdentifier": "some-string",
        "name": "some-string",
        "description": "some-string",
        "position": 42,
        "active": true,
        "availabilityRuleId": "some-string",
        "mediaId": "some-string",
        "formattedHandlerIdentifier": "some-string"
    },
    "shippingMethod": {
        "name": "some-string",
        "active": true,
        "description": "some-string",
        "trackingUrl": "some-string",
        "deliveryTimeId": "some-string",
        "availabilityRuleId": "some-string",
        "mediaId": "some-string"
    },
    "shippingLocation": [],
    "context": {
        "versionId": "some-string",
        "currencyId": "some-string",
        "currencyFactor": 42,
        "currencyPrecision": 42,
        "scope": "some-string",
        "source": "some-string",
        "taxState": "some-string",
        "useCache": true
    }
}
```

Read the context

### HTTP Request

`GET http://example.com/store-api/v3/context`
## updateContext

> **Responses**



> 200 - Context

```json
{
    "contextToken": "some-string"
}
```

Update the context

### HTTP Request

`PATCH http://example.com/store-api/v3/context`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**currencyId** | string |  | no | Currency
**languageId** | string |  | no | Language
**billingAddressId** | string |  | no | Billing Address
**shippingAddressId** | string |  | no | Shipping Address
**paymentMethodId** | string |  | no | Payment Method
**shippingMethodId** | string |  | no | Shipping Method
**countryId** | string |  | no | Country
**countryStateId** | string |  | no | Country State

# /currency

## readCurrency

> **Responses**



> 200 - All available currency

```json
{
    "id": "some-string",
    "factor": "number",
    "symbol": "some-string",
    "isoCode": "some-string",
    "shortName": "some-string",
    "name": "some-string",
    "decimalPrecision": 42,
    "position": 42,
    "isSystemDefault": true,
    "customFields": "object",
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "translated": "object",
    "promotionDiscountPrices": "#\/components\/schemas\/promotion_discount_prices_flat"
}
```

Loads all available currency

### HTTP Request

`GET http://example.com/store-api/v3/currency`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON

# /language

## readLanguages

> **Responses**



> 200 - All available languages

```json
[]
```

Loads all available languages

### HTTP Request

`GET http://example.com/store-api/v3/language`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON

# /salutation

## readSalutation

> **Responses**



> 200 - 

```json
[]
```

Salutations

### HTTP Request

`POST http://example.com/store-api/v3/salutation`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON

# /country

## readCountry

> **Responses**



> 200 - All available countries

```json
[]
```

Loads all available countries

### HTTP Request

`GET http://example.com/store-api/v3/country`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON
**onlyAvailable** | int | query | no | Encoded SwagQL in JSON

# /product/{id}/cross-selling

# /category/{categoryId}

## readCategory

> **Responses**



> 200 - The loaded category with cms page

```json
{
    "id": "some-string",
    "versionId": "some-string",
    "parentId": "some-string",
    "parentVersionId": "some-string",
    "afterCategoryId": "some-string",
    "afterCategoryVersionId": "some-string",
    "mediaId": "some-string",
    "displayNestedProducts": true,
    "autoIncrement": 42,
    "breadcrumb": [],
    "level": 42,
    "path": "some-string",
    "childCount": 42,
    "type": "some-string",
    "visible": true,
    "active": true,
    "name": "some-string",
    "customFields": "object",
    "slotConfig": "object",
    "externalLink": "some-string",
    "description": "some-string",
    "metaTitle": "some-string",
    "metaDescription": "some-string",
    "keywords": "some-string",
    "cmsPageId": "some-string",
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "translated": "object",
    "parent": "#\/components\/schemas\/category_flat",
    "children": "#\/components\/schemas\/category_flat",
    "media": "#\/components\/schemas\/media_flat",
    "products": "#\/components\/schemas\/product_flat",
    "nestedProducts": "#\/components\/schemas\/product_flat",
    "tags": "#\/components\/schemas\/tag_flat",
    "cmsPage": "#\/components\/schemas\/cms_page_flat",
    "mainCategories": "#\/components\/schemas\/main_category_flat",
    "seoUrls": "#\/components\/schemas\/seo_url_flat"
}
```

> 404 - 



Loads a category with the resolved cms page

### HTTP Request

`POST http://example.com/store-api/v3/category/{categoryId}`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON
**categoryId** | string | query | no | Id of the category

# /navigation/{requestActiveId}/{requestRootId}

## readNavigation

> **Responses**



> 200 - All available navigations

```json
[]
```

Loads all available navigations

### HTTP Request

`GET http://example.com/store-api/v3/navigation/{requestActiveId}/{requestRootId}`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON
**buildTree** | boolean | query | no | Build category tree

# /product-listing/{categoryId}

## readProductListing

> **Responses**



> 200 - Found products

```json
{
    "apiAlias": "some-string",
    "sorting": "some-string",
    "page": 42,
    "limit": 42,
    "elements": []
}
```

Loads products from listing

### HTTP Request

`POST http://example.com/store-api/v3/product-listing/{categoryId}`
# /search

## searchPage

> **Responses**



> 200 - Found products

```json
{
    "apiAlias": "some-string",
    "sorting": "some-string",
    "page": 42,
    "limit": 42,
    "elements": []
}
```

Search

### HTTP Request

`GET http://example.com/store-api/v3/search`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**search** | string | query | no | Search term

# /search-suggest

## searchSuggest

> **Responses**



> 200 - Found products

```json
{
    "apiAlias": "some-string",
    "sorting": "some-string",
    "page": 42,
    "limit": 42,
    "elements": []
}
```

Search suggests

### HTTP Request

`GET http://example.com/store-api/v3/search-suggest`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**search** | string | query | no | Search term

# /cms/{id}

## readCms

> **Responses**



> 200 - The loaded cms page

```json
{
    "id": "some-string",
    "name": "some-string",
    "type": "some-string",
    "entity": "some-string",
    "config": {
        "backgroundColor": "some-string"
    },
    "previewMediaId": "some-string",
    "customFields": "object",
    "locked": true,
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "translated": "object",
    "sections": "#\/components\/schemas\/cms_section_flat",
    "previewMedia": "#\/components\/schemas\/media_flat",
    "categories": "#\/components\/schemas\/category_flat"
}
```

> 404 - 



Resolves a cms page

### HTTP Request

`POST http://example.com/store-api/v3/cms/{id}`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON

# /contact-form

## sendContactMail

> **Responses**



> 200 - Message sent



Send message throught contact form

### HTTP Request

`POST http://example.com/store-api/v3/contact-form`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**salutationId** | string | body | no | Salutation ID
**firstName** | string | body | no | Firstname
**lastName** | string | body | no | Lastname
**email** | string | body | no | Email
**phone** | string | body | no | Phone
**subject** | string | body | no | Title
**comment** | string | body | no | Message

# /newsletter/confirm

## confirmNewsletter

> **Responses**



> 200 - Success



Confirm newsletter registration

### HTTP Request

`POST http://example.com/store-api/v3/newsletter/confirm`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**hash** | string | query | no | Hash from Mail
**em** | string | query | no | Hash from Mail

# /newsletter/subscribe

## subscribeToNewsletter

> **Responses**



> 200 - Success



Subscribe to newsletter

### HTTP Request

`POST http://example.com/store-api/v3/newsletter/subscribe`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**email** | string | query | no | Email
**salutationId** | string | query | no | Salutation
**firstName** | string | query | no | Firstname
**lastName** | string | query | no | Lastname
**street** | string | query | no | Street
**city** | string | query | no | City
**zipCode** | string | query | no | Zipcode

# /newsletter/unsubscribe

## unsubscribeToNewsletter

> **Responses**



> 200 - Success



Unsubscribe to newsletter

### HTTP Request

`POST http://example.com/store-api/v3/newsletter/unsubscribe`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**email** | string | query | no | Email

# /seo-url

## readSeoUrl

> **Responses**



> 200 - Found seo urls

```json
[]
```

> 404 - 



Loads seo urls

### HTTP Request

`POST http://example.com/store-api/v3/seo-url`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON

# /checkout/cart

## readCart

> **Responses**



> 200 - Cart

```json
{
    "name": "some-string",
    "token": "some-string",
    "price": {
        "netPrice": "number",
        "totalPrice": "number",
        "positionPrice": "number",
        "taxStatus": "some-string"
    },
    "lineItems": [],
    "errors": [],
    "deliveries": [],
    "transactions": [],
    "modified": true,
    "customerComment": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "data": []
}
```

Fetch current cart

### HTTP Request

`GET http://example.com/store-api/v3/checkout/cart`
## deleteCart

> **Responses**



Delete the cart

### HTTP Request

`DELETE http://example.com/store-api/v3/checkout/cart`
# /handle-payment

## handlePaymentMethod

> **Responses**



> 200 - Redirect to external payment provider



Handles a payment for an order

### HTTP Request

`GET http://example.com/store-api/v3/handle-payment`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**orderId** | string | post | yes | The id of the order
**finishUrl** | string | post | no | URL to which the external payment provider should redirect after successful payment
**errorUrl** | string | post | no | URL to which the external payment provider should redirect after erroneous payment

# /payment-method

## readPaymentMethod

> **Responses**



> 200 - All available payment methods

```json
[]
```

Loads all available payment methods

### HTTP Request

`GET http://example.com/store-api/v3/payment-method`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON
**onlyAvailable** | int | query | no | Encoded SwagQL in JSON

# /shipping-method

## readShippingMethod

> **Responses**



> 200 - All available shipping methods

```json
[]
```

Loads all available shipping methods

### HTTP Request

`GET http://example.com/store-api/v3/shipping-method`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON
**onlyAvailable** | int | query | no | Encoded SwagQL in JSON

# /account/change-profile

## changeProfile

> **Responses**



> 200 - 

```json
{
    "success": true
}
```

Change profile information

### HTTP Request

`POST http://example.com/store-api/v3/account/change-profile`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**salutationId** | string | body | no | Salutation
**fistName** | string | body | no | Firstname
**lastName** | string | body | no | Lastname

# /account/change-email

## changeEmail

> **Responses**



> 200 - 

```json
{
    "success": true
}
```

Change email

### HTTP Request

`POST http://example.com/store-api/v3/account/change-email`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**email** | string | body | no | New Email
**emailConfirmation** | string | body | no | New Email
**password** | string | body | no | Current password

# /account/change-password

## changePassword

> **Responses**



> 200 - 

```json
{
    "success": true
}
```

Change password

### HTTP Request

`POST http://example.com/store-api/v3/account/change-password`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**password** | string | body | no | Current password
**newPassword** | string | body | no | New password
**newPasswordConfirm** | string | body | no | New password

# /account/change-payment-method/{paymentMethodId}

## changePaymentMethod

> **Responses**



> 200 - 

```json
{
    "success": true
}
```

Change payment method

### HTTP Request

`POST http://example.com/store-api/v3/account/change-payment-method/{paymentMethodId}`
# /account/customer

## readCustomer

> **Responses**



> 200 - Loggedin customer

```json
{
    "id": "some-string",
    "groupId": "some-string",
    "defaultPaymentMethodId": "some-string",
    "salesChannelId": "some-string",
    "languageId": "some-string",
    "lastPaymentMethodId": "some-string",
    "defaultBillingAddressId": "some-string",
    "defaultShippingAddressId": "some-string",
    "autoIncrement": 42,
    "customerNumber": "some-string",
    "salutationId": "some-string",
    "firstName": "some-string",
    "lastName": "some-string",
    "company": "some-string",
    "email": "some-string",
    "title": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "active": true,
    "doubleOptInRegistration": true,
    "doubleOptInEmailSentDate": "some-string",
    "doubleOptInConfirmDate": "some-string",
    "hash": "some-string",
    "guest": true,
    "firstLogin": "some-string",
    "lastLogin": "some-string",
    "newsletter": true,
    "birthday": "some-string",
    "lastOrderDate": "some-string",
    "orderCount": 42,
    "customFields": "object",
    "remoteAddress": "some-string",
    "tagIds": [],
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "group": "#\/components\/schemas\/customer_group_flat",
    "defaultPaymentMethod": "#\/components\/schemas\/payment_method_flat",
    "salesChannel": "#\/components\/schemas\/sales_channel_flat",
    "language": "#\/components\/schemas\/language_flat",
    "lastPaymentMethod": "#\/components\/schemas\/payment_method_flat",
    "defaultBillingAddress": "#\/components\/schemas\/customer_address_flat",
    "defaultShippingAddress": "#\/components\/schemas\/customer_address_flat",
    "salutation": "#\/components\/schemas\/salutation_flat",
    "addresses": "#\/components\/schemas\/customer_address_flat",
    "orderCustomers": "#\/components\/schemas\/order_customer_flat",
    "tags": "#\/components\/schemas\/tag_flat",
    "promotions": "#\/components\/schemas\/promotion_flat",
    "productReviews": "#\/components\/schemas\/product_review_flat",
    "recoveryCustomer": "#\/components\/schemas\/customer_recovery_flat"
}
```

Returns informations about the loggedin customer

### HTTP Request

`GET http://example.com/store-api/v3/account/customer`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON

# /account/login

## loginCustomer

> **Responses**



> 200 - Context token

```json
{
    "contextToken": "some-string"
}
```

Login as customer using password

### HTTP Request

`POST http://example.com/store-api/v3/account/login`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**Email** | string | body | no | Email
**Password** | string | body | no | Password

# /account/logout

## logoutCustomer

> **Responses**



> 200 - 



Logouts current loggedin customer

### HTTP Request

`POST http://example.com/store-api/v3/account/logout`
# /account/register-confirm

## registerConfirm

> **Responses**



> 200 - Success



Confirm double optin registration

### HTTP Request

`POST http://example.com/store-api/v3/account/register-confirm`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**hash** | string | query | no | Hash from Link in Mail
**em** | string | query | no | em from Link in Mail

# /account/register

## register

> **Responses**



> 200 - Success

```json
{
    "id": "some-string",
    "groupId": "some-string",
    "defaultPaymentMethodId": "some-string",
    "salesChannelId": "some-string",
    "languageId": "some-string",
    "lastPaymentMethodId": "some-string",
    "defaultBillingAddressId": "some-string",
    "defaultShippingAddressId": "some-string",
    "autoIncrement": 42,
    "customerNumber": "some-string",
    "salutationId": "some-string",
    "firstName": "some-string",
    "lastName": "some-string",
    "company": "some-string",
    "email": "some-string",
    "title": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "active": true,
    "doubleOptInRegistration": true,
    "doubleOptInEmailSentDate": "some-string",
    "doubleOptInConfirmDate": "some-string",
    "hash": "some-string",
    "guest": true,
    "firstLogin": "some-string",
    "lastLogin": "some-string",
    "newsletter": true,
    "birthday": "some-string",
    "lastOrderDate": "some-string",
    "orderCount": 42,
    "customFields": "object",
    "remoteAddress": "some-string",
    "tagIds": [],
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "group": "#\/components\/schemas\/customer_group_flat",
    "defaultPaymentMethod": "#\/components\/schemas\/payment_method_flat",
    "salesChannel": "#\/components\/schemas\/sales_channel_flat",
    "language": "#\/components\/schemas\/language_flat",
    "lastPaymentMethod": "#\/components\/schemas\/payment_method_flat",
    "defaultBillingAddress": "#\/components\/schemas\/customer_address_flat",
    "defaultShippingAddress": "#\/components\/schemas\/customer_address_flat",
    "salutation": "#\/components\/schemas\/salutation_flat",
    "addresses": "#\/components\/schemas\/customer_address_flat",
    "orderCustomers": "#\/components\/schemas\/order_customer_flat",
    "tags": "#\/components\/schemas\/tag_flat",
    "promotions": "#\/components\/schemas\/promotion_flat",
    "productReviews": "#\/components\/schemas\/product_review_flat",
    "recoveryCustomer": "#\/components\/schemas\/customer_recovery_flat"
}
```

Register

### HTTP Request

`POST http://example.com/store-api/v3/account/register`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**guest** | boolean | query | no | Create guest user
**title** | string | query | no | Title
**salutationId** | string | query | no | Salutation
**firstName** | string | query | no | Firstname
**lastName** | string | query | no | Lastname
**email** | string | query | no | email
**affiliateCode** | string | query | no | Affilicate Code
**campaignCode** | string | query | no | Campaign Code
**password** | string | query | no | Password
**billingAddress** | #/components/schemas/customer_address_flat | query | no | Billingaddress
**shippingAddress** | #/components/schemas/customer_address_flat | query | no | Shippingaddress

# /account/recovery-password-confirm

## recoveryPassword

> **Responses**



> 200 - 



Resets password using recovery hash

### HTTP Request

`POST http://example.com/store-api/v3/account/recovery-password-confirm`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**hash** | string | body | no | Hash from confirmation mail
**newPassword** | string | body | no | new password
**newPasswordConfirm** | string | body | no | new password
**storefrontUrl** | string | body | no | baseurl for the url in mail

# /account/recovery-password

## sendRecoveryMail

> **Responses**



> 200 - 

```json
{
    "success": true
}
```

Sends a recovery email for password recovery

### HTTP Request

`POST http://example.com/store-api/v3/account/recovery-password`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**email** | string | body | no | Email
**storefrontUrl** | string | body | no | baseurl for the url in mail

# /order/state/cancel

## cancelOrder

> **Responses**



> 200 - 

```json
{
    "id": "some-string",
    "technicalName": "some-string",
    "name": "some-string",
    "stateMachineId": "some-string",
    "customFields": "object",
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "translated": "object",
    "stateMachine": "#\/components\/schemas\/state_machine_flat",
    "fromStateMachineTransitions": "#\/components\/schemas\/state_machine_transition_flat",
    "toStateMachineTransitions": "#\/components\/schemas\/state_machine_transition_flat",
    "orderTransactions": "#\/components\/schemas\/order_transaction_flat",
    "orderDeliveries": "#\/components\/schemas\/order_delivery_flat",
    "orders": "#\/components\/schemas\/order_flat",
    "toStateMachineHistoryEntries": "#\/components\/schemas\/state_machine_history_flat",
    "fromStateMachineHistoryEntries": "#\/components\/schemas\/state_machine_history_flat"
}
```

Cancel a order

### HTTP Request

`POST http://example.com/store-api/v3/order/state/cancel`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**orderId** | string | post | yes | The id of the order to be changed

# /order

## readOrder

> **Responses**



> 200 - 

```json
[]
```

Listing orders

### HTTP Request

`POST http://example.com/store-api/v3/order`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**page** | integer | query | no | page
**limit** | integer | query | no | Limit
**term** | string | query | no | The term to search for
**filter** | string | query | no | Encoded SwagQL in JSON
**post-filter** | string | query | no | Encoded SwagQL in JSON
**associations** | string | query | no | Encoded SwagQL in JSON
**aggregations** | string | query | no | Encoded SwagQL in JSON
**query** | string | query | no | Encoded SwagQL in JSON
**grouping** | string | query | no | Encoded SwagQL in JSON
**checkPromotion** | boolean | get | no | wether to check the Promotions of orders

# /order/set-payment

## orderSetPayment

> **Responses**



> 200 - 



set payment for an order

### HTTP Request

`POST http://example.com/store-api/v3/order/set-payment`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**paymentMethodId** | string | post | yes | The id of the paymentMethod to be set
**orderId** | string | post | yes | The id of the order

# /checkout/cart/line-item

## addLineItem

> **Responses**



> 200 - Cart

```json
{
    "name": "some-string",
    "token": "some-string",
    "price": {
        "netPrice": "number",
        "totalPrice": "number",
        "positionPrice": "number",
        "taxStatus": "some-string"
    },
    "lineItems": [],
    "errors": [],
    "deliveries": [],
    "transactions": [],
    "modified": true,
    "customerComment": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "data": []
}
```

Add new line item entries

### HTTP Request

`POST http://example.com/store-api/v3/checkout/cart/line-item`
## removeLineItem

> **Responses**



> 200 - Cart

```json
{
    "name": "some-string",
    "token": "some-string",
    "price": {
        "netPrice": "number",
        "totalPrice": "number",
        "positionPrice": "number",
        "taxStatus": "some-string"
    },
    "lineItems": [],
    "errors": [],
    "deliveries": [],
    "transactions": [],
    "modified": true,
    "customerComment": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "data": []
}
```

Remove line item entries

### HTTP Request

`DELETE http://example.com/store-api/v3/checkout/cart/line-item`
## updateLineItem

> **Responses**



> 200 - Cart

```json
{
    "name": "some-string",
    "token": "some-string",
    "price": {
        "netPrice": "number",
        "totalPrice": "number",
        "positionPrice": "number",
        "taxStatus": "some-string"
    },
    "lineItems": [],
    "errors": [],
    "deliveries": [],
    "transactions": [],
    "modified": true,
    "customerComment": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "data": []
}
```

Update line item entries

### HTTP Request

`PATCH http://example.com/store-api/v3/checkout/cart/line-item`
# /checkout/order

## createOrder

> **Responses**



> 200 - Order

```json
{
    "id": "some-string",
    "versionId": "some-string",
    "autoIncrement": 42,
    "orderNumber": "some-string",
    "billingAddressId": "some-string",
    "billingAddressVersionId": "some-string",
    "currencyId": "some-string",
    "languageId": "some-string",
    "salesChannelId": "some-string",
    "orderDateTime": "some-string",
    "orderDate": "some-string",
    "price": {
        "netPrice": "number",
        "totalPrice": "number",
        "calculatedTaxes": "object",
        "taxRules": "object",
        "positionPrice": "number",
        "taxStatus": "some-string"
    },
    "amountTotal": "number",
    "amountNet": "number",
    "positionPrice": "number",
    "taxStatus": "some-string",
    "shippingCosts": {
        "unitPrice": "number",
        "totalPrice": "number",
        "quantity": 42,
        "calculatedTaxes": "object",
        "taxRules": "object",
        "referencePrice": "object",
        "listPrice": {
            "price": "number",
            "discount": "number",
            "percentage": "number"
        }
    },
    "shippingTotal": "number",
    "currencyFactor": "number",
    "deepLinkCode": "some-string",
    "affiliateCode": "some-string",
    "campaignCode": "some-string",
    "customerComment": "some-string",
    "stateId": "some-string",
    "customFields": "object",
    "createdAt": "some-string",
    "updatedAt": "some-string",
    "stateMachineState": "#\/components\/schemas\/state_machine_state_flat",
    "orderCustomer": "#\/components\/schemas\/order_customer_flat",
    "currency": "#\/components\/schemas\/currency_flat",
    "language": "#\/components\/schemas\/language_flat",
    "addresses": "#\/components\/schemas\/order_address_flat",
    "deliveries": "#\/components\/schemas\/order_delivery_flat",
    "lineItems": "#\/components\/schemas\/order_line_item_flat",
    "transactions": "#\/components\/schemas\/order_transaction_flat",
    "documents": "#\/components\/schemas\/document_flat",
    "tags": "#\/components\/schemas\/tag_flat"
}
```

Create a new order from cart

### HTTP Request

`POST http://example.com/store-api/v3/checkout/order`
# /pwa/page

## pwaPage

> **Responses**



> 200 - The loaded cms page

```json
{
    "resourceType": "some-string",
    "resourceIdentifier": "some-string",
    "canonicalPathInfo": "some-string",
    "cmsPage": "#\/components\/schemas\/cms_page_flat"
}
```

> 404 - Page not found



Resolves a given URL to its corresponding CMS page and hydrates it with content.

### HTTP Request

`POST http://example.com/store-api/v3/pwa/page`
### Parameters:

Parameter | Type | In | Required | Description
----- | ----- | -----| ----- | -----
**path** | string | post | yes | Path of the page to be returned
**includes** | object | post | no | Includes object to define sparse responses.

