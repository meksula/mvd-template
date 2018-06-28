---
title: API reference
permalink: /docs/mdreference/
---

Here you can find list of endpoints with description, request parameters and HTTP method.
Check code samples for find out how to execute request.

### Resources creation

A list of endpoints that are intended to resource creation.

#### Registration

<i>Use this endpoint if you want to register as the creator of content in the service. You will receive a message with your data on the email you typed.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/registration`
* Parameters: 
	- String username
	- String password
	- String name
	- String surname
	- String email
	- int age

#### Account verification

<i>Use this endpoint if you want to verify your registration. As parameters, enter data from your mailbox.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/verification`
* Parameters:
	- String spotMakerId
	- String verificationCode

#### Spot creation

<i>Use this endpoint if you want to create a new that can be viewed and visited by users.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot`
* Parameters:
	- String name
	- String description
	- boolean searchEnable
	- String city
	- String street
	- String buildingNumber
	
#### Picture sending

<i>Upload a picture of the place you created. This will allow for a better reputation and recognition!</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/{spotId}`
* Parameters:
	- String spotId [here past spotId of Spot created by you]
	- A file with `.jpg` extension

<hr>
### Resources exploration 

Exploration of resources created before by common user.

#### Explorer personalization

<i>Optionally, you can send your data to the server. If you log in using OAuth2 we do not have your data, but you can personalize your profile.</i>
* Method: `PUT`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/explorer/personalization`
* Parameters:
	- String nickname
	- String email
	- String name
	- String surname

#### Find nearest Spot

<i>This endpoint will find the closest Spot to visit.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/nearest`
* Parameters:
	- double lat
	- double lng

#### Find Spot in your current city

<i>This endpoint will find all Spots to visit in city where you are now.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/city`
* Parameters:
	- double lat
	- double lng

#### Find Spot in your current district

<i>This endpoint will find all Spots to visit in district where you are now.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/district`
* Parameters:
	- double lat
	- double lng

#### Find top Spot in your country

<i>This endpoint will find top Spots to visit in your country. You can specify a number of Spots.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/top/{amount}`
* Parameters:
	- int amount [here type an amount of spot]

#### Find Spot by spotId

<i>Use this endpoint to find Spot by spotId.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/{spotId}`
* Parameters:
	- String spotId [here type a spotId]

#### Visit Spot

<i>Use this endpoint to find Spot by spotId.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration`
* Parameters:
	- String spotId
	- String explorerId

#### Get visits history of Explorer

<i>Use the endpoint if you want to visit specified Spot.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/history/{explorerId}`
* Parameters:
	- String explorerId

#### Get Spot's average rate

<i>Returns the average rating of a place.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/exploration/{spotId}/rate`
* Parameters:
	- String spotId

#### Add opinion

<i>Use the endpoint to send your opinion to a specific Spot.</i>
* Method: `POST`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/opinions`
* Parameters:
	- String explorerId
	- String spotId
	- double rate
	- String content

#### Get latest opinions

<i>Get recently added opinions. Specify the number of entities.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/opinions/latest/{spotId}/{amount}`
* Parameters:
	- String spotId
	- double amount

#### Get best opinions

<i>Get best opinions of Spot. Specify the number of entities.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/opinions/best/{spotId}/{amount}`
* Parameters:
	- String spotId
	- double amount

#### Get worst opinions

<i>Get worst opinions of Spot. Specify the number of entities.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/opinions/worst/{spotId}/{amount}`
* Parameters:
	- String spotId
	- double amount

#### Get eplorer's opinions

<i>Get all opinions you've added. Specify the number of entities.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/opinions/explorer/{explorerId}`
* Parameters:
	- String spotId
	- double amount

#### Get all Spot's opinions

<i>Get all opinions of Spot by spotId.</i>
* Method: `GET`
* Endpoint URL: `http://51.38.129.50:8085/api/v1/spot/opinions/all/{spotId}`
* Parameters:
	- String spotId




















