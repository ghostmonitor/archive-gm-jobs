# GHOSTMONITOR PHP Junior - Weather forecast api
1. Create a Rest api in Laravel (4 or 5) with the following endpoints
2. _Bonus: write tests_
3. _Bonus: Create a Rest api in Nodejs with the following endpoints

__Submit your your code through `bitbucket.org` creating a private!!! repo and adding the following users: `pigri`, `barczaG`__ 

_Please also provide setup / deploy instructions along with your code_

## `GET` /current_temperature

Return the current temperature (in celsius) in budapest

* **Example response :**

  * **Code:** 200 <br />
    **Content:** `{ temp : 18 }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/current_temperature",
      dataType: "json",
      type : "GET",
      success : function(r) {
        console.log(r);
      }
    });
  ```

## `POST` /email_temperature

Send the current temperature to the specified email address

*  **Body Params**

   -to : recipient email address

* **Example response :**

  * **Code:** 200 <br />
    **Content:** `{ status : 'ok' }`

* **Sample Call:**

  ```javascript
    $.ajax({
      url: "/email_temperature",
      dataType: "json",
      data: {
        to: 'gergo@ghostmonitor.com'
      }
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
  ```


## `POST` /subscribe_temperature

Send the current temperature to the specified email address __in every hour__

*  **Body Params**

   -to : recipient email address

* **Example response :**

  * **Code:** 200 <br />
    **Content:** `{ status : 'ok' }`

```javascript
    $.ajax({
      url: "/subscribe_temperature",
      dataType: "json",
      data: {
        to: 'gergo@ghostmonitor.com'
      }
      type : "POST",
      success : function(r) {
        console.log(r);
      }
    });
