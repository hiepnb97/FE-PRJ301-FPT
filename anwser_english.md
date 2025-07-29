# FE PRJ301 FPT - SPRING 2025 - Đáp án

**1. What's the point of using `<fmt:setLocale>` in a JSP?** 
* **A. To pick the main language for the website.** 
* **B. To tell other tags which language and country format to use.** 
* **C. To change the user's language settings.** 
* **D. To choose the language for database information.** 

**Trả lời:** B. Để cho các thẻ khác biết định dạng ngôn ngữ và quốc gia nào sẽ sử dụng. 

**Giải thích:** Thẻ `<fmt:setLocale>` trong JSP được sử dụng để thiết lập ngôn ngữ (locale) hiện tại cho các thẻ định dạng khác (như `<fmt:formatNumber>`, `<fmt:formatDate>`) trong trang JSP. Nó giúp kiểm soát cách hiển thị số, ngày, tiền tệ, v.v., theo một ngôn ngữ và quốc gia cụ thể.

**2. In Java web applications, which of the following URL patterns is commonly used in `<servlet-mapping>` to indicate that a servlet should handle requests for all URLs in a specific directory and its subdirectories?** 
* **A** 
* **B. /servlet/** 
* **C. .html** 
* **D. /pages/\*** 

**Trả lời:** D. /pages/\* 

**Giải thích:** Trong `<servlet-mapping>` của file `web.xml`, mẫu URL `/pages/*` được sử dụng để khớp với tất cả các yêu cầu đến bất kỳ URL nào bắt đầu bằng `/pages/`, bao gồm cả các thư mục con. Ví dụ, nó sẽ khớp với `/pages/index.html`, `/pages/users/profile.jsp`, v.v.

**3. What functionality does the `doTag()` method provide in a custom tag handler?** 
* **A. It connects to a database to retrieve data.** 
* **B. It specifies the custom tag's output to the JSP page.** 
* **C. It sets the HTTP headers for the response.** 
* **D. It parses XML content within the custom tag.** 

**Trả lời:** B. Nó chỉ định đầu ra của thẻ tùy chỉnh vào trang JSP. 

**Giải thích:** Phương thức `doTag()` trong một `SimpleTagSupport` (thường được sử dụng cho custom tag handlers) là nơi logic chính của thẻ tùy chỉnh được thực thi và nơi nội dung được tạo ra và ghi vào `JspWriter` để xuất ra trang JSP.

**4. What is the purpose of the `contextDestroyed(ServletContextEvent sce)` method in a `ServletContextListener`?** 
* **A. To initialize servlets in the web application.** 
* **B. To handle exceptions thrown during servlet initialization.** 
* **C. To clean up resources when the web application is shutting down.** 
* **D. To manage session expiration and removal.** 

**Trả lời:** C. Để dọn dẹp tài nguyên khi ứng dụng web đang tắt. 

**Giải thích:** Phương thức `contextDestroyed()` của `ServletContextListener` được gọi khi ứng dụng web bị hủy (ví dụ, khi máy chủ bị tắt hoặc ứng dụng được triển khai lại). Đây là nơi thích hợp để giải phóng các tài nguyên đã được cấp phát trong `contextInitialized()`, chẳng hạn như đóng kết nối cơ sở dữ liệu hoặc giải phóng bộ nhớ.

**5. Which of the followings is a correct syntax of the method that is used to get the initialized parameter in ServletContext or ServletConfig?** 
* **A. String getInitializedParameter(String name)** 
* **B. String getInitParameter(String name)** 
* **C. String getContextParameter(String name)** 
* **D. String getBoolParameter(String name)** 

**Trả lời:** B. String getInitParameter(String name) 

**Giải thích:** Cả `ServletContext` và `ServletConfig` đều cung cấp phương thức `getInitParameter(String name)` để truy xuất giá trị của một tham số khởi tạo (initialization parameter) được định nghĩa trong `web.xml` hoặc thông qua chú thích `@WebInitParam`.

**6. Which attribute of the `<tag>` element is used to specify the name of the custom tag?** 
* **A. name** 
* **B. class** 
* **C. body-content** 
* **D. description** 

**Trả lời:** A. name 

**Giải thích:** Trong TLD (Tag Library Descriptor) file, thuộc tính `name` của phần tử `<tag>` được sử dụng để định nghĩa tên của thẻ tùy chỉnh. Tên này sau đó sẽ được sử dụng trong JSP để gọi thẻ, ví dụ: `<myprefix:name>`.

**7. How can a Simple Tag Handler access the body content of the custom tag?** 
* **A. By using the 'getWriter() method of the JspWriter class.** 
* **B. By implementing the BodyTag interface in the tag handler class.** 
* **C. By using the getJspContext().getOut() method of the "JspContext class.** 
* **D. By using the 'getParent() method of the javax.servlet.jsp.tagext. Tag interface.** 

**Trả lời:** C. Bằng cách sử dụng phương thức `getJspContext().getOut()` của lớp `JspContext`. 

**Giải thích:** `SimpleTagHandler` sử dụng phương thức `getJspBody()` để lấy `JspFragment` đại diện cho phần thân của thẻ. Sau đó, `JspFragment` có thể được gọi với một `Writer` để xử lý và xuất nội dung phần thân. `getJspContext().getOut()` cung cấp `JspWriter` để ghi nội dung ra trang JSP, và thường được dùng kết hợp với `getJspBody().invoke(null)` hoặc `getJspBody().invoke(getJspContext().getOut())` để xử lý body content.

**8. When multiple filters are applied to a servlet, what determines the order of execution?** 
* **A. The order in which the filters are defined in the web.xml file.** 
* **B. The filter's priority attribute** 
* **C. The order in which the filters were added to the web application.** 
* **D. The servlet's URL pattern.** 

**Trả lời:** A. Thứ tự các bộ lọc được định nghĩa trong tệp web.xml. 

**Giải thích:** Trong các ứng dụng web Java EE, thứ tự thực thi của các bộ lọc được xác định bởi thứ tự chúng được khai báo trong tệp `web.xml` (hoặc thứ tự các chú thích `@WebFilter` được quét, nếu sử dụng cấu hình dựa trên chú thích).

**9. Which is NOT a component of the MVC architecture in Java web frameworks?** 
* **A. Service Layer** 
* **B. Model** 
* **C. View** 
* **D. Controller** 

**Trả lời:** A. Service Layer 

**Giải thích:** Kiến trúc MVC (Model-View-Controller) bao gồm ba thành phần chính:
* **Model:** Đại diện cho dữ liệu và logic nghiệp vụ.
* **View:** Đại diện cho giao diện người dùng và cách hiển thị dữ liệu.
* **Controller:** Xử lý các yêu cầu của người dùng, tương tác với Model và chọn View phù hợp để hiển thị.
Service Layer không phải là một thành phần cốt lõi của MVC, mà thường là một phần của Model hoặc một lớp nằm giữa Controller và Model để tổ chức logic nghiệp vụ.

**10. What is the first method called when a filter is initialized in a web application?** 
* **A. initFilter()** 
* **B. initialize()** 
* **C. init()** 
* **D. setupFilter()** 

**Trả lời:** C. init() 

**Giải thích:** Khi một bộ lọc (Filter) được khởi tạo bởi bộ chứa servlet, phương thức `init(FilterConfig filterConfig)` của nó sẽ được gọi đầu tiên. Phương thức này được sử dụng để thực hiện các thao tác khởi tạo một lần cho bộ lọc.

**11. What is MVC architecture?**
* **A. Multi-View Controller**
* **B. Module-View-Controller**
* **C. Model-View-Controller**
* **D. Model-Value-Configuration**

**Trả lời:** C. Model-View-Controller

**Giải thích:** MVC là viết tắt của Model-View-Controller, một mẫu kiến trúc phần mềm được sử dụng rộng rãi để phát triển giao diện người dùng.

**12. How does the GET method handle sensitive data compared to the POST method?**
* **A. GET encrypts data ensuring secure transmission**
* **B. POST is more suitable for secure data transfer**
* **C. GET exposes sensitive data in the URL**
* **D. GET can handle larger data volumes than POST**

**Trả lời:** C. GET hiển thị dữ liệu nhạy cảm trong URL.

**Giải thích:** Phương thức GET truyền dữ liệu dưới dạng các tham số trong chuỗi truy vấn của URL, làm cho dữ liệu có thể nhìn thấy được trong lịch sử trình duyệt, nhật ký máy chủ và dễ bị tấn công. Ngược lại, POST gửi dữ liệu trong phần thân của yêu cầu HTTP, an toàn hơn cho dữ liệu nhạy cảm.

**13. Which method is called when a servlet is being removed from service?**
* **A. destroy()**
* **B. stop()**
* **C. end()**
* **D. dispose()**

**Trả lời:** A. destroy()

**Giải thích:** Phương thức `destroy()` của một servlet được gọi bởi bộ chứa servlet khi servlet đó bị xóa khỏi dịch vụ, thường là khi ứng dụng web bị tắt hoặc hủy triển khai. Đây là nơi để giải phóng bất kỳ tài nguyên nào mà servlet đã giữ.

**14. What purpose does a logging filter serve in a Java web application?**
* **A. Modifies the content of a response.**
* **B. Logs requests and responses for monitoring**
* **C. Manages session timeouts**
* **D. Redirects requests to different servers**

**Trả lời:** B. Ghi nhật ký các yêu cầu và phản hồi để giám sát.

**Giải thích:** Một bộ lọc ghi nhật ký (logging filter) được thiết kế để chặn các yêu cầu và phản hồi HTTP, sau đó ghi lại thông tin về chúng (như URL yêu cầu, địa chỉ IP, thời gian phản hồi, v.v.) vào một tệp nhật ký hoặc hệ thống giám sát. Mục đích chính là để theo dõi và gỡ lỗi ứng dụng.

**15. When is the `contextInitialized()` method of a `ServletContextListener` invoked?**
* **A. After the web server receives an HTTP request**
* **B. When a new session is created for a client**
* **C. When the web application is deployed or started**
* **D. After the response is sent back to the client**

**Trả lời:** C. Khi ứng dụng web được triển khai hoặc khởi động.

**Giải thích:** Phương thức `contextInitialized(ServletContextEvent sce)` của `ServletContextListener` được gọi một lần duy nhất khi ứng dụng web được khởi động thành công (triển khai). Đây là nơi lý tưởng để thực hiện các thao tác khởi tạo toàn cầu cho ứng dụng.

**16. You are tasked with improving the performance of a JSP MVC application which currently experiences slow page loading times. Propose a strategy for optimizing the application, considering MVC principles.**
* **A. Increase the server's hardware capacity to handle more concurrent requests**
* **B. Implement caching mechanisms within the View to store rendered pages**
* **C. Optimize database queries within the Model to reduce data retrieval times**
* **D. Minimize the use of MVC architecture and revert to a monolithic design for performance**

**Trả lời:** C. Tối ưu hóa các truy vấn cơ sở dữ liệu trong Model để giảm thời gian truy xuất dữ liệu.

**Giải thích:** Trong kiến trúc MVC, Model chịu trách nhiệm về dữ liệu và logic nghiệp vụ. Thời gian tải trang chậm thường liên quan đến việc truy xuất dữ liệu kém hiệu quả. Việc tối ưu hóa các truy vấn cơ sở dữ liệu trong Model (ví dụ: tối ưu hóa SQL, sử dụng chỉ mục, giảm số lượng truy vấn) sẽ trực tiếp cải thiện hiệu suất của ứng dụng.

**17. How can you include another JSP file within a JSP page?**
* **A. Using the `<import>` tag.**
* **B. Using the `<%@ include %>` directive.**
* **C. Using the `<link>` tag.**
* **D. Using the `<external>` tag.**

**Trả lời:** B. Bằng cách sử dụng chỉ thị `<%@ include %>`.

**Giải thích:** Chỉ thị `<%@ include file="file.jsp" %>` được sử dụng để đưa nội dung của một tệp JSP khác vào trang JSP hiện tại tại thời điểm dịch (translation time). Điều này có nghĩa là nội dung của tệp được đưa vào sẽ được biên dịch cùng với tệp JSP chính.

**18. How can you create a drop down list in an HTML form?**
* **A. By using the `<dropdown>` element.**
* **B. By using the `<list>` element.**
* **C. By using the `<select>` element.**
* **D. By using the `<options>` element.**

**Trả lời:** C. Bằng cách sử dụng phần tử `<select>`.

**Giải thích:** Trong HTML, phần tử `<select>` được sử dụng để tạo một danh sách thả xuống. Các tùy chọn trong danh sách được định nghĩa bằng các phần tử `<option>` bên trong thẻ `<select>`.

**19. How are sessions typically identified on the server side in web development?**
* **A. IP address of the client**
* **B. User-agent string**
* **C. Session ID**
* **D. Server-generated random token**

**Trả lời:** C. ID phiên.

**Giải thích:** Các phiên (sessions) trên phía máy chủ thường được xác định bằng một ID phiên (Session ID) duy nhất. ID này được tạo bởi máy chủ và thường được gửi đến máy khách dưới dạng cookie hoặc được thêm vào URL (URL rewriting) để máy khách gửi lại trong các yêu cầu tiếp theo, cho phép máy chủ theo dõi trạng thái của phiên.

**20. Which of the following is true about HTTP Get method?**
* **A. Called by the server (via the service method) to allow a servlet to handle a GET request.**
* **B. The GET method is the default method to pass information from browser to web server.**
* **C. Both of the above**
* **D. None of the above**

**Trả lời:** C. Cả hai điều trên đều đúng.

**Giải thích:**
* **A.** Phương thức `doGet()` trong servlet được gọi bởi phương thức `service()` (mà phương thức `service()` lại được gọi bởi bộ chứa servlet) để xử lý các yêu cầu HTTP GET.
* **B.** Khi bạn nhập một URL vào trình duyệt hoặc nhấp vào một liên kết, theo mặc định, trình duyệt sẽ gửi một yêu cầu HTTP GET đến máy chủ web.

**21. Which JSTL core tag is used to output a value onto the JSP page?**
* **A. `<c:out>`**
* **B. `<c:display>`**
* **C. `<c:print>`**
* **D. `<c:value>`**

**Trả lời:** A. `<c:out>`

**Giải thích:** Thẻ `<c:out>` trong thư viện thẻ lõi JSTL được sử dụng để xuất giá trị của một biểu thức hoặc biến ra trang JSP. Nó cũng cung cấp khả năng thoát (escape) các ký tự đặc biệt của HTML để ngăn chặn các cuộc tấn công XSS.

**22. Which implicit object provides access to HTTP headers and cookies in a Java Servlet?**
* **A. request**
* **B. response**
* **C. session**
* **D. application**

**Trả lời:** A. request

**Giải thích:** Đối tượng `HttpServletRequest` (được truy cập thông qua đối tượng ngầm định `request` trong JSP hoặc là tham số `req` trong phương thức `doGet`/`doPost` của servlet) cung cấp các phương thức để truy cập các tiêu đề HTTP (ví dụ: `getHeader()`) và cookie (ví dụ: `getCookies()`) từ yêu cầu của máy khách.

**23. What is the correct order of the servlet life cycle phases?**
* **A. Initialization, Service, Destroy**
* **B. Service, Initialization, Destroy**
* **C. Destroy, Service, Initialization**
* **D. Initialization, Destroy, Service**

**Trả lời:** A. Initialization, Service, Destroy

**Giải thích:** Vòng đời của một servlet bao gồm ba giai đoạn chính theo thứ tự:
1.  **Initialization (Khởi tạo):** Phương thức `init()` được gọi một lần khi servlet được khởi tạo.
2.  **Service (Phục vụ):** Phương thức `service()` (hoặc `doGet()`, `doPost()`, v.v.) được gọi cho mỗi yêu cầu đến servlet.
3.  **Destroy (Hủy bỏ):** Phương thức `destroy()` được gọi một lần khi servlet bị xóa khỏi dịch vụ.

**24. When does HttpSessionListener's `sessionCreated` method get invoked?**
* **A. When a user submits a form**
* **B. When a new session is created**
* **C. When the servlet context is initialized**
* **D. When a session is invalidated**

**Trả lời:** B. Khi một phiên mới được tạo.

**Giải thích:** Phương thức `sessionCreated(HttpSessionEvent se)` của `HttpSessionListener` được gọi bởi bộ chứa web ngay sau khi một phiên HTTP mới được tạo ra cho một máy khách.

**25. In a JSP error page, how can you access the exception object thrown by the server?**
* **A. By using the `<error>` tag.**
* **B. By using the implicit object `exception`.**
* **C. By using the implicit object `error`.**
* **D. By using the `<exception>` tag.**

**Trả lời:** B. Bằng cách sử dụng đối tượng ngầm định `exception`.

**Giải thích:** Khi một trang JSP được chỉ định là trang lỗi (thông qua thuộc tính `errorPage` của trang JSP khác hoặc cấu hình `<error-page>` trong `web.xml`), nó sẽ có quyền truy cập vào đối tượng ngầm định `exception`, đại diện cho ngoại lệ đã được ném ra.

**26. Where is the deployment descriptor located?**
* **A. The deployment descriptor is located in the WEB-INF directory of the web application.**
* **B. The deployment descriptor is located in the WEB-INFS directory of the web application.**
* **C. The deployment descriptor is located in the WEBS-INF directory of the web application.**
* **D. The deployment descriptor is located in the WEBS directory of the web application.**

**Trả lời:** A. Tệp mô tả triển khai nằm trong thư mục WEB-INF của ứng dụng web.

**Giải thích:** Tệp mô tả triển khai, thường là `web.xml`, phải được đặt trong thư mục `WEB-INF` của ứng dụng web. Thư mục `WEB-INF` là một thư mục đặc biệt không thể truy cập trực tiếp từ máy khách và chứa các tệp cấu hình và lớp Java của ứng dụng.

**27. How does DBMS deal with concurrent multi-user?**
* **A. Connection pool is provided by DBMS server and application server.**
* **B. Using 1 connection shared by multi-user.**
* **C. Eliminate connection leaks in database applications.**
* **D. Always manage database tasks with transaction.**

**Trả lời:** A. Nhóm kết nối (Connection pool) được cung cấp bởi máy chủ DBMS và máy chủ ứng dụng.

**Giải thích:** Để xử lý đa người dùng đồng thời một cách hiệu quả, hệ quản trị cơ sở dữ liệu (DBMS) và máy chủ ứng dụng thường sử dụng nhóm kết nối (connection pool). Nhóm kết nối duy trì một tập hợp các kết nối cơ sở dữ liệu sẵn sàng để sử dụng, giúp giảm chi phí tạo và đóng kết nối cho mỗi yêu cầu, từ đó cải thiện hiệu suất và khả năng mở rộng.

**28. In a Java Servlet, what is the purpose of the `doPost()` method?**
* **A. Handling HTTP GET requests**
* **B. Handling HTTP POST requests**
* **C. Handling HTTP PUT requests**
* **D. Handling HTTP DELETE requests**

**Trả lời:** B. Xử lý các yêu cầu HTTP POST.

**Giải thích:** Phương thức `doPost(HttpServletRequest req, HttpServletResponse resp)` trong một Java Servlet được thiết kế đặc biệt để xử lý các yêu cầu HTTP POST được gửi từ máy khách.

**29. What is NOT a valid JDBC Statement type?**
* **A. BatchStatement**
* **B. PreparedStatement**
* **C. CallableStatement**
* **D. Statement**

**Trả lời:** A. BatchStatement

**Giải thích:** Trong JDBC, các kiểu `Statement` hợp lệ là:
* `Statement`: Dùng để thực thi các câu lệnh SQL tĩnh.
* `PreparedStatement`: Dùng để thực thi các câu lệnh SQL đã được biên dịch trước và có thể có tham số.
* `CallableStatement`: Dùng để gọi các thủ tục lưu trữ (stored procedures) trong cơ sở dữ liệu.
`BatchStatement` không phải là một kiểu `Statement` chuẩn trong JDBC. Tuy nhiên, JDBC hỗ trợ xử lý theo lô (batch processing) thông qua các phương thức `addBatch()` và `executeBatch()` có sẵn trên các đối tượng `Statement`, `PreparedStatement` và `CallableStatement`.

**30. What syntax is used to denote an EL expression in a JSP page?**
* **A. ${}**
* **B. #{}**
* **C. @{}**
* **D. %{}**

**Trả lời:** A. ${}

**Giải thích:** Biểu thức ngôn ngữ (Expression Language - EL) trong JSP được bao bọc bởi cú pháp `${}`. Ví dụ: `${user.name}` sẽ truy cập thuộc tính `name` của đối tượng `user`.

**31. Which of the following statements best describes the role of JDBC in web applications?**
* **A. JDBC is used to create dynamic web pages**
* **B. JDBC is a protocol for transferring data between web servers and browsers**
* **C. JDBC is a standard Java API for interacting with databases**
* **D. JDBC is a web server for serving Java applications**

**Trả lời:** C. JDBC là một API Java tiêu chuẩn để tương tác với cơ sở dữ liệu.

**Giải thích:** JDBC (Java Database Connectivity) là một API (Application Programming Interface) của Java, cung cấp một phương tiện tiêu chuẩn để các ứng dụng Java kết nối và tương tác với các cơ sở dữ liệu quan hệ.

**32. Which status code is returned when a request cannot be fulfilled due to bad syntax?**
* **A. 500**
* **B. 400**
* **C. 404**
* **D. 302**

**Trả lời:** B. 400

**Giải thích:** Mã trạng thái HTTP 400 Bad Request cho biết rằng máy chủ không thể xử lý yêu cầu do có lỗi cú pháp không hợp lệ từ phía máy khách.

**33. Which JSP element is NOT executed at the service() method of the servlet?**
* **A. Scriptlet**
* **B. Expression**
* **C. Declaration**
* **D. Directive**

**Trả lời:** D. Directive

**Giải thích:**
* **Scriptlet (`<% ... %>`)** và **Expression (`<%= ... %>`)** được dịch thành mã Java bên trong phương thức `_jspService()` của servlet được tạo ra từ JSP, và do đó được thực thi khi phương thức `service()` được gọi.
* **Declaration (`<%! ... %>`)** được dịch thành các thành viên (biến hoặc phương thức) của lớp servlet được tạo ra, nằm ngoài phương thức `_jspService()`.
* **Directive (`<%@ ... %>`)** là các chỉ thị được xử lý tại thời điểm dịch (translation time) của JSP, trước khi servlet được biên dịch và do đó không được thực thi bên trong phương thức `service()`.

**34. What is the ServletContext in a Java web application?**
* **A. An object representing a single servlet instance**
* **B. An interface for interacting with the client's web browser**
* **C. An object representing the entire web application**
* **D. A mechanism for managing session data**

**Trả lời:** C. Một đối tượng đại diện cho toàn bộ ứng dụng web.

**Giải thích:** `ServletContext` là một đối tượng duy nhất cho mỗi ứng dụng web được triển khai trên một bộ chứa servlet. Nó cung cấp quyền truy cập vào các tham số khởi tạo cấp ứng dụng, các thuộc tính chung, và cho phép giao tiếp giữa các servlet trong cùng một ứng dụng.

**35. What is the purpose of using database transactions in a web application with multiple database operations?**
* **A. To ensure all operations are executed simultaneously.**
* **B. To group operations together as a single unit of work.**
* **C. To increase the likelihood of data corruption.**
* **D. To decrease database performance.**

**Trả lời:** B. Để nhóm các thao tác lại với nhau thành một đơn vị công việc duy nhất.

**Giải thích:** Giao dịch cơ sở dữ liệu (database transaction) được sử dụng để nhóm một hoặc nhiều thao tác cơ sở dữ liệu lại với nhau thành một đơn vị công việc logic. Điều này đảm bảo tính toàn vẹn của dữ liệu bằng cách đảm bảo rằng tất cả các thao tác trong giao dịch đều thành công (commit) hoặc tất cả đều thất bại (rollback), tuân theo các thuộc tính ACID.

**36. Which file is commonly used to specify deployment descriptors and configurations for a Java web application?**
* **A. web.config**
* **B. web.xml**
* **C. app.properties**
* **D. deployment.ini**

**Trả lời:** B. web.xml

**Giải thích:** Tệp `web.xml` (Deployment Descriptor) là tệp cấu hình trung tâm cho các ứng dụng web Java EE (Java Servlet). Nó chứa thông tin về các servlet, bộ lọc, trình nghe, ánh xạ URL, tham số khởi tạo, trang lỗi và nhiều cấu hình khác cho ứng dụng web.

**37. Which is NOT a standard technique for a session to be definitely invalidated?**
* **A. The container is shutdown and brought up again**
* **B. No request comes from the client for more than "session timeout" period**
* **C. If the session time out is set to 0 using `setMaxInactiveInterval()` method**
* **D. A servlet explicitly calls `invalidate()` on a session object.**

**Trả lời:** C. Nếu thời gian chờ phiên được đặt thành 0 bằng cách sử dụng phương thức `setMaxInactiveInterval()`.

**Giải thích:**
* **A.** Khi container bị tắt hoặc khởi động lại, tất cả các phiên sẽ bị hủy bỏ.
* **B.** Nếu không có hoạt động nào từ máy khách trong khoảng thời gian `maxInactiveInterval` (thời gian chờ phiên), phiên sẽ tự động hết hạn.
* **D.** Gọi `session.invalidate()` sẽ hủy bỏ phiên ngay lập tức.
* **C.** Nếu `setMaxInactiveInterval()` được đặt thành 0, phiên sẽ không bao giờ hết hạn tự động; nó chỉ bị hủy bỏ khi trình duyệt đóng hoặc khi `invalidate()` được gọi rõ ràng. Do đó, đây KHÔNG phải là một kỹ thuật để phiên bị hủy bỏ "chắc chắn" trong trường hợp không có hoạt động.

**38. How is the EL expression `${user.name}` executed in JSP?**
* **A. It calls `user.getName()`**
* **B. It accesses the name property of the user object**
* **C. It is a scriptlet**
* **D. It is a declaration**

**Trả lời:** B. Nó truy cập thuộc tính tên của đối tượng người dùng.

**Giải thích:** Biểu thức EL `${user.name}` sử dụng cơ chế introspection (phản chiếu) để truy cập thuộc tính `name` của đối tượng `user`. Điều này thường được thực hiện bằng cách tìm kiếm phương thức `getName()` hoặc một trường công khai có tên `name`. EL tự động xử lý việc gọi phương thức getter.

**39. What is the correct syntax for accessing the length of a String stored in a request attribute named "message" using EL?**
* **A. ${message.length}**
* **B. ${requestScope.message.size}**
* **C. ${message.length()}**
* **D. ${fn:length(message)}**

**Trả lời:** D. ${fn:length(message)}

**Giải thích:** Để lấy độ dài của một chuỗi trong EL, bạn cần sử dụng hàm `length()` từ thư viện hàm JSTL (thường được tiền tố là `fn`). Cú pháp đúng là `${fn:length(message)}`.

**40. What is the purpose of the `pattern` attribute in the `<fmt:formatNumber>` tag?**
* **A. To specify the language of the formatted number.**
* **B. To define the number format pattern.**
* **C. To set the currency symbol.**
* **D. To set the time zone for the formatting.**

**Trả lời:** B. Để xác định mẫu định dạng số.

**Giải thích:** Thuộc tính `pattern` trong thẻ `<fmt:formatNumber>` của JSTL được sử dụng để cung cấp một chuỗi mẫu định dạng số (ví dụ: "###,##0.00" cho định dạng số có dấu phẩy và hai chữ số thập phân).

**41. What is URL rewriting in the context of web applications?**
* **A. A technique for obfuscating URLs to prevent unauthorized access**
* **B. A method of redirecting users to different web pages**
* **C. A mechanism for appending session information to URLs**
* **D. A process of compressing URLs to improve website performance**

**Trả lời:** C. Một cơ chế để thêm thông tin phiên vào URL.

**Giải thích:** URL rewriting là một kỹ thuật trong đó một ID phiên (Session ID) được thêm vào URL khi cookie bị vô hiệu hóa hoặc không được hỗ trợ bởi trình duyệt. Điều này cho phép máy chủ theo dõi phiên của người dùng bằng cách truyền ID phiên trong chính URL cho mỗi yêu cầu.

**42. Which structure of Status Line In Response Message is**
* **A. [HTTP Version] [Response Code] [Status]**
* **B. [HTTP Method] [Protocol Version] [Requested Resource forming URI]**
* **C. [HTTP Version] [Response Code] [Http Method]**
* **D. [HTTP Version] [Protocol Code] [Http Method]**

**Trả lời:** A. [HTTP Version] [Response Code] [Status]

**Giải thích:** Dòng trạng thái (Status Line) của một phản hồi HTTP có cấu trúc: `HTTP-Version Status-Code Reason-Phrase`. Trong các lựa chọn, "[HTTP Version] [Response Code] [Status]" là cách diễn giải gần nhất với cấu trúc chuẩn, trong đó "Status" tương ứng với `Reason-Phrase`.

**43. Which Java statement does the `<c:when>` tag within `<c:choose>` resemble?**
* **A. if**
* **B. while**
* **C. for**
* **D. switch-case**

**Trả lời:** D. switch-case

**Giải thích:** Các thẻ `<c:choose>`, `<c:when>`, và `<c:otherwise>` trong JSTL hoạt động tương tự như một cấu trúc `switch-case` trong Java. Thẻ `<c:choose>` bắt đầu khối, mỗi thẻ `<c:when>` đại diện cho một trường hợp (`case`), và thẻ `<c:otherwise>` là trường hợp mặc định (`default`).

**44. What does the `<rtexprvalue>` element specify in the TLD?**
* **A. The return type of the custom tag handler class with runtime**
* **B. Whether the attribute can accept runtime expressions.**
* **C. The body content type of the custom tag.**
* **D. The tag handler class.**

**Trả lời:** B. Liệu thuộc tính có thể chấp nhận các biểu thức thời gian chạy hay không.

**Giải thích:** Trong tệp mô tả thư viện thẻ (Tag Library Descriptor - TLD), phần tử `<rtexprvalue>` (runtime expression value) trong định nghĩa `<attribute>` được sử dụng để chỉ định xem thuộc tính của thẻ tùy chỉnh có thể chấp nhận một biểu thức kịch bản (scriptlet expression) hoặc biểu thức EL (Expression Language) tại thời gian chạy hay không. Nếu là `true`, bạn có thể truyền các giá trị động cho thuộc tính đó.

**45. What is NOT the use of filter in JSP?**
* **A. Authentication blocking request based on user identity**
* **B. Logging and auditing - Tracking uses of a web application**
* **C. Image Conversion - Scaling maps and so on**
* **D. Link to my bootstrap.min.css in a JSP file**
* **E. Data Compression - Making downloads smaller**

**Trả lời:** D. Liên kết đến tệp bootstrap.min.css trong tệp JSP.

**Giải thích:** Bộ lọc (Filter) trong các ứng dụng web Java được sử dụng để chặn và xử lý các yêu cầu và phản hồi HTTP trước khi chúng đến servlet hoặc sau khi chúng rời khỏi servlet. Các mục đích sử dụng phổ biến bao gồm:
* Xác thực (Authentication) và ủy quyền (Authorization)
* Ghi nhật ký (Logging) và kiểm toán (Auditing)
* Chuyển đổi dữ liệu, bao gồm cả nén hoặc chuyển đổi định dạng
Việc liên kết đến tệp CSS (như `bootstrap.min.css`) là một nhiệm vụ của JSP hoặc HTML, không phải là chức năng của bộ lọc.

**46. What is NOT the use of filter in JSP?**
* **A. Authentication blocking request based on user identity**
* **B. Logging and auditing - Tracking uses of a web application**
* **C. Image Conversion - Scaling maps and so on**
* **D. Link to my bootstrap.min.css in a JSP file**
* **E. Data Compression - Making downloads smaller**

**Trả lời:** D. Liên kết đến tệp bootstrap.min.css trong tệp JSP.

**Giải thích:** Câu hỏi này lặp lại câu hỏi trước. Bộ lọc (Filter) trong các ứng dụng web Java được sử dụng để chặn và xử lý các yêu cầu và phản hồi HTTP trước khi chúng đến servlet hoặc sau khi chúng rời khỏi servlet. Các mục đích sử dụng phổ biến bao gồm:
* Xác thực (Authentication) và ủy quyền (Authorization)
* Ghi nhật ký (Logging) và kiểm toán (Auditing)
* Chuyển đổi dữ liệu, bao gồm cả nén hoặc chuyển đổi định dạng
Việc liên kết đến tệp CSS (như `bootstrap.min.css`) là một nhiệm vụ của JSP hoặc HTML, không phải là chức năng của bộ lọc.

**47. In a multi-tier data model, which layer is responsible for handling application logic?**
* **A. User Interface/Application Layer**
* **B. Application Logic Layer**
* **C. Data Layer**
* **D. Connection Layer**

**Trả lời:** B. Tầng logic ứng dụng.

**Giải thích:** Trong kiến trúc đa tầng (multi-tier architecture), tầng logic ứng dụng (Application Logic Layer), còn được gọi là tầng nghiệp vụ (Business Layer), chịu trách nhiệm chứa và thực thi các quy tắc nghiệp vụ, logic xử lý và các phép tính chính của ứng dụng.

**48. In a standard Java web application, where is the deployment descriptor (web.xml) typically located?**
* **A. WEB-INF**
* **B. META-INF**
* **C. WEB-INF/classes**
* **D. Root directory**

**Trả lời:** A. WEB-INF

**Giải thích:** Tệp `web.xml`, là tệp mô tả triển khai của ứng dụng web Java, luôn được đặt trong thư mục `WEB-INF` của cấu trúc thư mục ứng dụng web.

**49. During which method call are the JSP's form data and cookies available?**
* **A. jspInit()**
* **B. _jspService()**
* **C. jspDestroy()**
* **D. jspDoStart()**

**Trả lời:** B. _jspService()

**Giải thích:** Phương thức `_jspService()` là phương thức chính được tạo ra bởi bộ chứa servlet từ một JSP. Phương thức này tương ứng với phương thức `service()` của một servlet thông thường và là nơi các yêu cầu được xử lý. Do đó, các đối tượng `request` và `response` (bao gồm dữ liệu biểu mẫu và cookie) có sẵn trong phương thức này.

**50. What does a session listener do in a web application?**
* **A. It listens to and records conversations**
* **B. It watches for changes in user sessions, like when someone logs in or out**
* **C. It changes session data**
* **D. It helps users navigate the application**

**Trả lời:** B. Nó theo dõi các thay đổi trong phiên người dùng, giống như khi ai đó đăng nhập hoặc đăng xuất.

**Giải thích:** Một trình nghe phiên (session listener), cụ thể là `HttpSessionListener`, được sử dụng để theo dõi các sự kiện trong vòng đời của phiên HTTP, chẳng hạn như khi một phiên được tạo (`sessionCreated`) hoặc bị hủy bỏ (`sessionDestroyed`). Điều này hữu ích cho việc quản lý tài nguyên hoặc ghi nhật ký các hoạt động liên quan đến phiên.

**51. What syntax does EL use to access an element in a list?**
* **A. ${list[index]}**
* **B. ${list.get(index)}**
* **C. ${list(index)}**
* **D. ${list.element[index]}**

**Trả lời:** A. ${list[index]}

**Giải thích:** Trong Expression Language (EL), bạn có thể truy cập các phần tử của một `List` hoặc mảng bằng cách sử dụng toán tử dấu ngoặc vuông `[]` với chỉ số. Ví dụ: `${list[0]}` sẽ truy cập phần tử đầu tiên của danh sách.