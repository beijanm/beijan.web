---
toc: false
comments: false 
layout: post
title: Delete Function
type: hacks
courses: { compsci: {week: 20} }
---

<!-- 
A simple HTML login form with a Login action when button is pressed.  

The form triggers the login_user function defined in the JavaScript below when the Login button is pressed.
-->

<form action="javascript:delete_user()">
    <h2><label>
        User ID:
        <input type="text" name="duid" id="duid" required>
    </label></h2>
    <p>
        <button class="delete-button">Delete</button>
        <button onClick = "window.location.href ='http://127.0.0.1:4200/beijan.web//2024/01/31/Login.html'" class="button-spacing" >Login</button>
    </p>

</form>

<script type="module">
    // uri variable and options object are obtained from config.js
    import { uri, options } from 'http://127.0.0.1:8086/assets/js/api/config.js';

    const url = uri + '/api/users/';

    function delete(){
    const body = {
      uid: document.getElementById("duid").value,
    };
    const AuthOptions = {
                mode: 'cors', // no-cors, *cors, same-origin
                credentials: 'include', // include, same-origin, omit
                headers: {
                    'Content-Type': 'application/json',
                },
                method: 'DELETE', // Override the method property
                cache: 'no-cache', // Set the cache property
                body: JSON.stringify(body) // delete if using backend code that fetches directly from the cookie
            };
      // fetch the API
      fetch(url, AuthOptions)
        // response is a RESTful "promise" on any successful fetch
        .then(response => {
          // check for response errors and display
          if (response.status !== 200) {
                window.location.replace("http://127.0.0.1:8086/403_Error?message=Insufficient+Permissions");
                return;
          }
          // valid response will contain JSON data
          response.json().then(data => {
            window.location.href = "http://127.0.0.1:8086/data/database";
          })
      })
      // catch fetch errors (ie ACCESS to server blocked)
      .catch(err => {
        console.log(err)
      });
  }
  window.delete_user = delete;
</script>