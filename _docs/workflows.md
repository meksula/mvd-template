---
title: Workflows
permalink: /docs/workflows/
---

Here's an example workflow for an API that allows you to perform basic API operations.

### SpotMaker registration

First of all, you must be authenticated in the service.

1. In `POST` request you should send JSON object that contains parameters like: `String username`, `String password`, `String name`,`String surname`,`String email`, `int age`.
<br>API endpoint: `[HOSTNAME]/api/v1/registration`

2. Go to your mail and read the email you received.
<br>You will have two codes: `spotMakerId` and `verificationCode`

3. Execute next `POST` request in order to verification your e-mail account.
<br> This request should has parameters: `spotMakerId`, `verificationCode`
<br>API endpoint: `[HOSTNAME]/api/v1/verification`

Look at code samples
Congratulations, you've been just registered in Smart Explorer API.

### Create our first Spot

Spot is the main subject of application. Users (Explorer) can find it by their coordinates.
If you want to create new spot you don't have to know coordinates of your museum or something other.

1. Execute `POST` request with parameters: `String name`, `String description`, `boolean searchEnable`, `String city`, `String street`, `String buildingNumber`
<br>API endpoint: `[HOSTNAME]/api/v1/spot`

That is all application find coordinates of address and display for Explorers! 
Warn! If your Spot is in village as `street` type `city` again.

2. How find our spot? Execute `GET` request. You have to know spotId - replace it with {spotId}:
<br>API endpoint: `[HOSTNAME]/api/v1/spot/exploration/{spotId}`

3. Finally you should add a picture to your just created Spot.
<br>Do `POST` request that'll contain a file with extension `.jpg`.
To do this it's best to use Postman. But in <a href="http://localhost:4000/mvd-template/docs/code_samples/">code samples</a> you find out how to do this with cURL. 

Next features will describe soon.


