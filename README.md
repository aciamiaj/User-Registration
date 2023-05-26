# User-Registration

The code provided in this repository demonstrates a simple servlet implementation for handling user registration data from an HTML form.

## Usage
To use the User Registration, follow these steps:

Set up a Java web project and configure a Servlet container (e.g., Apache Tomcat) to run the servlet.

Create an HTML form to capture user registration data. Make sure to specify the form action as /registration to match the servlet URL mapping.

<form action="/registration" method="post">
    <!-- Form fields -->
</form>
Implement the doPost() method in the UserProcess servlet class to handle the form submission. The method retrieves the form parameters, performs validation, and generates an HTML response.

Deploy the servlet project to the Servlet container and access the registration form through a web browser.

Servlet Mapping
The UserProcess servlet is mapped to the /registration URL using the @WebServlet annotation.

@WebServlet("/registration")
public class UserProcess extends HttpServlet {
    // Servlet code
}
Make sure the servlet mapping matches the form action in your HTML form.

Form Validation
The servlet performs basic validation on the submitted form data. If any required fields are empty, an error message is displayed. Otherwise, a success message is displayed along with the submitted information.

HTML Response
The servlet generates an HTML response using a PrintWriter. The response includes dynamically generated HTML elements based on the submitted form data.

CSS Styling
The servlet assumes the existence of a CSS file named style.css for styling the HTML elements in the response. Make sure to include the appropriate CSS file in your project and reference it in the HTML response.

## Lifecycle Methods
The servlet contains the init() and destroy() methods, which are part of the servlet lifecycle. These methods are called by the Servlet container during servlet initialization and destruction. In the provided code, they simply print log messages when called.

## Dependencies
This project has the following dependencies:

Java Servlet API: Used for creating servlet classes and handling HTTP requests/responses.
