---
title: Get started
permalink: /docs/home/
redirect_from: /docs/index.html
---

**Welcome to the documentation for Smart Explorer API v1!**

Smart Explorer API v1 is a RESTful API that you can use to:

* create and propagate historical places (museum etc.)
* explore many places without any problem
* gather statistics about tourism industry

Smart Explorer API v1 uses HTTP protocol and HTTP method: `GET`, `POST`, `PUT`, and `DELETE`. Responses are returned only in JSON format.

To access Smart Explorer API v1, you'll need only email address. After registration you'll receive verification code that you have to send due to confirm your identity (read bellow).

For trial version there are no request limit etc.

## Authentication

Trial version has no API key or something similar.
To access API you have to register by simple way - HTTP Basic.

In Smart Explorer we have two types of users:
* SpotMaker -> able to create spots, read full statistics, rates and opinions
* Explorer -> common user able to search for spots, visit these and give rates and opinions

If you want to be only <b>Explorer</b> - just have an account on Facebook. Authentication oAuth2 is enough. You will be asked to allow the application to your basic data.

If you want to be <b>SpotMaker</b> `POST` your data to this endpoint: http://51.38.129.50:8085/api/v1/registration <br>
Further information and details you can find here <a href="http://localhost:4000/mvd-template/docs/workflows/">more</a>
