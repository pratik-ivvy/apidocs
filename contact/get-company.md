# Get Company

{% api-method method="post" host="\[PlatformAddress\]/api/1.0/contact?action=getCompany" path="" %}
{% api-method-summary %}
Get Company
{% endapi-method-summary %}

{% api-method-description %}
Get a single company's detail
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="integer" required=true %}
The company's identifier
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```text
{
  "id": "25146",
  "businessName": "Test",
  "tradingName": "Test Trading",
  "businessNumber": "1234586",
  "email": "company@test.com",
  "phone": "0455550000",
  "fax": "0455550125",
  "website": "www.test.com",
  "address": {
    "line1": "Street Number",
    "line2": "Street Name",
    "line3": "",
    "line4": "",
    "city": "Gold Coast",
    "stateCode": "QLD",
    "countryCode": "AU",
    "postalCode": "4227"
  }
  "primaryAccountManager": "Test User",
  "secondaryAccountManager": "Test User",
  "industry": "Industry Name",
  "primaryContact": "Test User",
  "agentcommission": {
      "commissionRoomHireValue": 123,
      "commissionRoomHireType": "CHF",
      "commissionFoodValue": 222,
      "commissionFoodType": "CHF",
      "commissionBeverageValue": 333,
      "commissionBeverageType": "CHF",
      "commissionAudioVisualValue": 444,
      "commissionAudioVisualType": "CHF",
      "commissionAccommodationValue": 555,
      "commissionAccommodationType": "CHF"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

## Example Request

`Get a specific company`

```javascript
{ 
  "id":6
}
```

## Returns

| Property | Description |
| :--- | :--- |
| id | The unique identifier for the company |
| externalId | Optionally a unique identifier of the company that is managed by an external application |
| businessName | The company's business name |
| tradingName | The company's trading name |
| businessNumber | The company's registration number |
| phone | The company's phone number |
| fax | The company's fax number |
| website | The company's website |
| email | The company's email address |
| address | The company’s address. This is an an object with the [keys](get-company.md#keys) |
| modifiedDate | The modified date of the company |
| primaryAccountManager | The primary account manager of the company. This is an an object with the [keys](get-company.md#primaryaccountmanager)  |
| secondaryAccountManager | The secondary account manager of the company. This is an an object with the [keys](get-company.md#secondaryaccountmanager)  |
| industry | The industry of the company. This is an an object with the [keys](get-company.md#industry)  |
| primaryContact | The primary contact of the company. This is an an object with the [keys](get-company.md#primarycontact) |
| commissionSpace | The commission amount of the company space.|
| commissionSpaceType | The commission amount type of the company space.|
| commissionFoodValue | The commission amount of the company food.|
| commissionFoodType | The commission amount type of the company food.|
| commissionBeverageValue | The commission amount of the company beverage.|
| commissionBeverageType | The commission amount type of the company beverage.|
| commissionAudioVisualValue | The commission amount of the company audio visual.|
| commissionAudioVisualType | The commission amount type of the company audio visual.|
| commissionAccommodationValue | The commission amount of the company accommodation.|
| commissionAccommodationType | The commission amount type of the accommodation.|

## Keys

| **keys** |
| :--- |
| line1 |
| line2 |
| line3 |
| line4 |
| city |
| stateCode \(e.g: QLD\) |
| countryCode \(e.g: AU\) |
| postalCode |

## primarycontact

| Property | Type | Description |
| :--- | :--- | :--- |
| id | integer | The unique identifier of the contact |
| firstName | string | The first name of the contact |
| lastName | string | The last name of the contact |
| email | string | The email address of the contact |
| phone | string | The phone number of the contact |

## primaryaccountmanager

| Property | Type | Description |
| :--- | :--- | :--- |
| id | integer | The unique identifier of the primary account manager |
| firstName | string | The first name of the primary account manager |
| lastName | string | The last name of the primary account manager |
| email | string | The email address of the primary account manager |

## secondaryaccountmanager

| Property | Type | Description |
| :--- | :--- | :--- |
| id | integer | The unique identifier of the secondary account manager |
| firstName | string | The first name of the secondary account manager |
| lastName | string | The last name of the secondary account manager |
| email | string | The email address of the secondary account manager |

## industry

| Property | Type | Description |
| :--- | :--- | :--- |
| id | integer | The unique identifier of the industry |
| name | string | The name of the industry |

## Throws

| Code | Description |
| :--- | :--- |
| Specific Code: 24153 | Unable to find company |

The company identifier must be provided to fetch a specific company from the system.

