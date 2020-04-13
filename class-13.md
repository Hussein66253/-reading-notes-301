# What is form data?
- **FormData** objects are used to capture HTML form and submit it using fetch or another network method. We can either create new **FormData(form)** from an HTML form, or create a object without a form at all, and then append fields with methods: **formData**
## The method attribute
 - The *method* attribute defines how data is sent. The **HTTP protoco**l provides several ways to perform a request; HTML form data can be transmitted via a number of different methods, the most common being the *GET* method and the *POST* method
## What is form data in::
-  **The POST method**:    
    - The HTTP **POST** method sends **data** to the server. The type of the body of the **request** is indicated by the Content-Type header. ... multipart/**form-data** : each value is sent as a block of **data** ("body part"), with a user agent-defined delimiter ("boundary") separating each part.
    - **The GET method**
    The **GET** method is the method used by the browser to ask the server to send back a given resource: "Hey server, I want to **GET** this resource." In this case, the browser sends an empty body. Because the body is empty, if a form is sent using this method the data sent to the server is appended to the URL.