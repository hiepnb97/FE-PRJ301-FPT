# FE PRJ301 FPT - SPRING 2025

## 📄 Đáp án:

- [Đáp án](answer_english.md)
- [Đáp án + Dịch tiếng Việt](answer_vietnamese.md)

## ❓ Câu hỏi:

**1. What's the point of using `<fmt:setLocale>` in a JSP?**
* A. To pick the main language for the website.
* B. To tell other tags which language and country format to use.
* C. To change the user's language settings.
* D. To choose the language for database information.

**2. In Java web applications, which of the following URL patterns is commonly used in `<servlet-mapping>` to indicate that a servlet should handle requests for all URLs in a specific directory and its subdirectories?**
* A
* B. /servlet/
* C. .html
* D. /pages/*

**3. What functionality does the `doTag()` method provide in a custom tag handler?**
* A. It connects to a database to retrieve data.
* B. It specifies the custom tag's output to the JSP page.
* C. It sets the HTTP headers for the response.
* D. It parses XML content within the custom tag.

**4. What is the purpose of the `contextDestroyed(ServletContextEvent sce)` method in a ServletContextListener?**
* A. To initialize servlets in the web application.
* B. To handle exceptions thrown during servlet initialization.
* C. To clean up resources when the web application is shutting down.
* D. To manage session expiration and removal.

**5. Which of the followings is a correct syntax of the method that is used to get the initialized parameter in ServletContext or ServletConfig?**
* A. String getInitializedParameter(String name)
* B. String getInitParameter(String name)
* C. String getContextParameter(String name)
* D. String g...

**6. Which attribute of the `<tag>` element is used to specify the name of the custom tag?**
* A. name
* B. class
* C. body-content
* D. description

**7. How can a Simple Tag Handler access the body content of the custom tag?**
* A. By using the 'getWriter() method of the JspWriter class.
* B. By implementing the BodyTag interface in the tag handler class.
* C. By using the getJspContext().getOut() method of the "JspContext class.
* D. By using the 'getParent() method of the javax.servlet.jsp.tagext. Tag interface.

**8. When multiple filters are applied to a servlet, what determines the order of execution?**
* A. The order in which the filters are defined in the web.xml file.
* B. The filter's priority attribute
* C. The order in which the filters were added to the web application.
* D. The servlet's URL pattern.

**9. Which is NOT a component of the MVC architecture in Java web frameworks?**
* A. Service Layer
* B. Model
* C. View
* D. Controller

**10. What is the first method called when a filter is initialized in a web application?**
* A. initFilter()
* B. initialize()
* C. init()
* D. setupFilter()

**11. What is MVC architecture?**
* A. Multi-View Controller
* B. Module-View-Controller
* C. Model-View-Controller
* D. Model-Value-Configuration

**12. How does the GET method handle sensitive data compared to the POST method?**
* A. GET encrypts data ensuring secure transmission
* B. POST is more suitable for secure data transfer
* C. GET exposes sensitive data in the URL
* D. GET can handle larger data volumes than POST

**13. Which method is called when a servlet is being removed from service?**
* A. destroy()
* B. stop()
* C. end()
* D. dispose()

**14. What purpose does a logging filter serve in a Java web application?**
* A. Modifies the content of a response.
* B. Logs requests and responses for monitoring
* C. Manages session timeouts
* D. Redirects requests to different servers

**15. When is the `contextInitialized()` method of a `ServletContextListener` invoked?**
* A. After the web server receives an HTTP request
* B. When a new session is created for a client
* C. When the web application is deployed or started
* D. After the response is sent back to the client

**16. You are tasked with improving the performance of a JSP MVC application which currently experiences slow page loading times. Propose a strategy for optimizing the application, considering MVC principles.**
* A. Increase the server's hardware capacity to handle more concurrent requests
* B. Implement caching mechanisms within the View to store rendered pages
* C. Optimize database queries within the Model to reduce data retrieval times
* D. Minimize the use of MVC architecture and revert to a monolithic design for performance

**17. How can you include another JSP file within a JSP page?**
* A. Using the `<import>` tag.
* B. Using the `<%@ include %>` directive.
* C. Using the `<link>` tag.
* D. Using the `<external>` tag.

**18. How can you create a drop down list in an HTML form?**
* A. By using the `<dropdown>` element.
* B. By using the `<list>` element.
* C. By using the `<select>` element.
* D. By using the `<options>` element.

**19. How are sessions typically identified on the server side in web development?**
* A. IP address of the client
* B. User-agent string
* C. Session ID
* D. Server-generated random token

**20. Which of the following is true about HTTP Get method?**
* A. Called by the server (via the service method) to allow a servlet to handle a GET request.
* B. The GET method is the default method to pass information from browser to web server.
* C. Both of the above
* D. None of the above

**21. Which JSTL core tag is used to output a value onto the JSP page?**
* A. `<c:out>`
* B. `<c:display>`
* C. `<c:print>`
* D. `<c:value>`

**22. Which implicit object provides access to HTTP headers and cookies in a Java Servlet?**
* A. request
* B. response
* C. session
* D. application

**23. What is the correct order of the servlet life cycle phases?**
* A. Initialization, Service, Destroy
* B. Service, Initialization, Destroy
* C. Destroy, Service, Initialization
* D. Initialization, Destroy, Service

**24. When does HttpSessionListener's `sessionCreated` method get invoked?**
* A. When a user submits a form
* B. When a new session is created
* C. When the servlet context is initialized
* D. When a session is invalidated

**25. In a JSP error page, how can you access the exception object thrown by the server?**
* A. By using the `<error>` tag.
* B. By using the implicit object `exception`.
* C. By using the implicit object `error`.
* D. By using the `<exception>` tag.

**26. Where is the deployment descriptor located?**
* A. The deployment descriptor is located in the WEB-INF directory of the web application.
* B. The deployment descriptor is located in the WEB-INFS directory of the web application.
* C. The deployment descriptor is located in the WEBS-INF directory of the web application.
* D. The deployment descriptor is located in the WEBS directory of the web application.

**27. How does DBMS deal with concurrent multi-user?**
* A. Connection pool is provided by DBMS server and application server.
* B. Using 1 connection shared by multi-user.
* C. Eliminate connection leaks in database applications.
* D. Always manage database tasks with transaction.

**28. In a Java Servlet, what is the purpose of the `doPost()` method?**
* A. Handling HTTP GET requests
* B. Handling HTTP POST requests
* C. Handling HTTP PUT requests
* D. Handling HTTP DELETE requests

**29. What is NOT a valid JDBC Statement type?**
* A. BatchStatement
* B. PreparedStatement
* C. CallableStatement
* D. Statement

**30. What syntax is used to denote an EL expression in a JSP page?**
* A. ${}
* B. #{}
* C. @{}
* D. %{}

**31. Which of the following statements best describes the role of JDBC in web applications?**
* A. JDBC is used to create dynamic web pages
* B. JDBC is a protocol for transferring data between web servers and browsers
* C. JDBC is a standard Java API for interacting with databases
* D. JDBC is a web server for serving Java applications

**32. Which status code is returned when a request cannot be fulfilled due to bad syntax?**
* A. 500
* B. 400
* C. 404
* D. 302

**33. Which JSP element is NOT executed at the service() method of the servlet?**
* A. Scriptlet
* B. Expression
* C. Declaration
* D. Directive

**34. What is the ServletContext in a Java web application?**
* A. An object representing a single servlet instance
* B. An interface for interacting with the client's web browser
* C. An object representing the entire web application
* D. A mechanism for managing session data

**35. What is the purpose of using database transactions in a web application with multiple database operations?**
* A. To ensure all operations are executed simultaneously.
* B. To group operations together as a single unit of work.
* C. To increase the likelihood of data corruption.
* D. To decrease database performance.

**36. Which file is commonly used to specify deployment descriptors and configurations for a Java web application?**
* A. web.config
* B. web.xml
* C. app.properties
* D. deployment.ini

**37. Which is NOT a standard technique for a session to be definitely invalidated?**
* A. The container is shutdown and brought up again
* B. No request comes from the client for more than "session timeout" period
* C. If the session time out is set to 0 using `setMaxInactiveInterval()` method
* D. A servlet explicitly calls `invalidate()` on a session object.

**38. How is the EL expression `${user.name}` executed in JSP?**
* A. It calls `user.getName()`
* B. It accesses the name property of the user object
* C. It is a scriptlet
* D. It is a declaration

**39. What is the correct syntax for accessing the length of a String stored in a request attribute named "message" using EL?**
* A. ${message.length}
* B. ${requestScope.message.size}
* C. ${message.length()}
* D. ${fn:length(message)}

**40. What is the purpose of the `pattern` attribute in the `<fmt:formatNumber>` tag?**
* A. To specify the language of the formatted number.
* B. To define the number format pattern.
* C. To set the currency symbol.
* D. To set the time zone for the formatting.

**41. What is URL rewriting in the context of web applications?**
* A. A technique for obfuscating URLs to prevent unauthorized access
* B. A method of redirecting users to different web pages
* C. A mechanism for appending session information to URLs
* D. A process of compressing URLs to improve website performance

**42. Which structure of Status Line In Response Message is**
* A. [HTTP Version] [Response Code] [Status]
* B. [HTTP Method] [Protocol Version] [Requested Resource forming URI]
* C. [HTTP Version] [Response Code] [Http Method]
* D. [HTTP Version] [Protocol Code] [Http Method]

**43. Which Java statement does the `<c:when>` tag within `<c:choose>` resemble?**
* A. if
* B. while
* C. for
* D. switch-case

**44. What does the `<rtexprvalue>` element specify in the TLD?**
* A. The return type of the custom tag handler class with runtime
* B. Whether the attribute can accept runtime expressions.
* C. The body content type of the custom tag.
* D. The tag handler class.

**45. What is NOT the use of filter in JSP?**
* A. Authentication blocking request based on user identity
* B. Logging and auditing - Tracking uses of a web application
* C. Image Conversion - Scaling maps and so on
* D. Link to my bootstrap.min.css in a JSP file
* E. Data Compression - Making downloads smaller

**46. What is NOT the use of filter in JSP?**
* A. Authentication blocking request based on user identity
* B. Logging and auditing - Tracking uses of a web application
* C. Image Conversion - Scaling maps and so on
* D. Link to my bootstrap.min.css in a JSP file
* E. Data Compression - Making downloads smaller

**47. In a multi-tier data model, which layer is responsible for handling application logic?**
* A. User Interface/Application Layer
* B. Application Logic Layer
* C. Data Layer
* D. Connection Layer

**48. In a standard Java web application, where is the deployment descriptor (web.xml) typically located?**
* A. WEB-INF
* B. META-INF
* C. WEB-INF/classes
* D. Root directory

**49. During which method call are the JSP's form data and cookies available?**
* A. jspInit()
* B. _jspService()
* C. jspDestroy()
* D. jspDoStart()

**50. What does a session listener do in a web application?**
* A. It listens to and records conversations
* B. It watches for changes in user sessions, like when someone logs in or out
* C. It changes session data
* D. It helps users navigate the application

**51. What syntax does EL use to access an element in a list?**
* A. ${list[index]}
* B. ${list.get(index)}
* C. ${list(index)}
* D. ${list.element[index]}

## 🖼️ Ảnh câu hỏi:

- [Câu hỏi 1](question_images/1.jpg)
- [Câu hỏi 2](question_images/2.jpg)
- [Câu hỏi 3](question_images/3.jpg)
- [Câu hỏi 4](question_images/4.jpg)
- [Câu hỏi 5](question_images/5.jpg)
- [Câu hỏi 6](question_images/6.jpg)
- [Câu hỏi 7](question_images/7.jpg)
- [Câu hỏi 8](question_images/8.jpg)
- [Câu hỏi 9](question_images/9.jpg)
- [Câu hỏi 10](question_images/10.jpg)
- [Câu hỏi 11](question_images/11.jpg)
- [Câu hỏi 12](question_images/12.jpg)
- [Câu hỏi 13](question_images/13.jpg)
- [Câu hỏi 14](question_images/14.jpg)
- [Câu hỏi 15](question_images/15.jpg)
- [Câu hỏi 16](question_images/16.jpg)
- [Câu hỏi 17](question_images/17.jpg)
- [Câu hỏi 18](question_images/18.jpg)
- [Câu hỏi 19](question_images/19.jpg)
- [Câu hỏi 20](question_images/20.jpg)
- [Câu hỏi 21](question_images/21.jpg)
- [Câu hỏi 22](question_images/22.jpg)
- [Câu hỏi 23](question_images/23.jpg)
- [Câu hỏi 24](question_images/24.jpg)
- [Câu hỏi 25](question_images/25.jpg)
- [Câu hỏi 26](question_images/26.jpg)
- [Câu hỏi 27](question_images/27.jpg)
- [Câu hỏi 28](question_images/28.jpg)
- [Câu hỏi 29](question_images/29.jpg)
- [Câu hỏi 30](question_images/30.jpg)
- [Câu hỏi 31](question_images/31.jpg)
- [Câu hỏi 32](question_images/32.jpg)
- [Câu hỏi 33](question_images/33.jpg)
- [Câu hỏi 34](question_images/34.jpg)
- [Câu hỏi 35](question_images/35.jpg)
- [Câu hỏi 36](question_images/36.jpg)
- [Câu hỏi 37](question_images/37.jpg)
- [Câu hỏi 38](question_images/38.jpg)
- [Câu hỏi 39](question_images/39.jpg)
- [Câu hỏi 40](question_images/40.jpg)
- [Câu hỏi 41](question_images/41.jpg)
- [Câu hỏi 42](question_images/42.jpg)
- [Câu hỏi 43](question_images/43.jpg)
- [Câu hỏi 44](question_images/44.jpg)
- [Câu hỏi 45](question_images/45.jpg)
- [Câu hỏi 46](question_images/46.jpg)
- [Câu hỏi 47](question_images/47.jpg)
- [Câu hỏi 48](question_images/48.jpg)
- [Câu hỏi 49](question_images/49.jpg)
- [Câu hỏi 50](question_images/50.jpg)
- [Câu hỏi 51](question_images/51.jpg)
