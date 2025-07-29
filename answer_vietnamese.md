# FE PRJ301 FPT - SPRING 2025 - Đáp án và dịch Tiếng Việt

**1. Điểm mấu chốt khi sử dụng `<fmt:setLocale>` trong JSP là gì?** 
* **A. Để chọn ngôn ngữ chính cho trang web.** 
* **B. Để cho các thẻ khác biết định dạng ngôn ngữ và quốc gia nào sẽ sử dụng.** 
* **C. Để thay đổi cài đặt ngôn ngữ của người dùng.** 
* **D. Để chọn ngôn ngữ cho thông tin cơ sở dữ liệu.** 

**Trả lời:** B. Để cho các thẻ khác biết định dạng ngôn ngữ và quốc gia nào sẽ sử dụng. 

**Giải thích:** Thẻ `<fmt:setLocale>` trong JSP được sử dụng để thiết lập ngôn ngữ (locale) hiện tại cho các thẻ định dạng khác (như `<fmt:formatNumber>`, `<fmt:formatDate>`) trong trang JSP. Nó giúp kiểm soát cách hiển thị số, ngày, tiền tệ, v.v., theo một ngôn ngữ và quốc gia cụ thể. 

**2. Trong các ứng dụng web Java, mẫu URL nào sau đây thường được sử dụng trong `<servlet-mapping>` để chỉ ra rằng một servlet sẽ xử lý các yêu cầu cho tất cả các URL trong một thư mục cụ thể và các thư mục con của nó?** 
* **A.** 
* **B. /servlet/** 
* **C. .html** 
* **D. /pages/\*** 

**Trả lời:** D. /pages/\* 

**Giải thích:** Trong `<servlet-mapping>` của file `web.xml`, mẫu URL `/pages/*` được sử dụng để khớp với tất cả các yêu cầu đến bất kỳ URL nào bắt đầu bằng `/pages/`, bao gồm cả các thư mục con. Ví dụ, nó sẽ khớp với `/pages/index.html`, `/pages/users/profile.jsp`, v.v.

**3. Phương thức `doTag()` cung cấp chức năng gì trong trình xử lý thẻ tùy chỉnh (custom tag handler)?** 
* **A. Nó kết nối với cơ sở dữ liệu để truy xuất dữ liệu.** 
* **B. Nó chỉ định đầu ra của thẻ tùy chỉnh vào trang JSP.** 
* **C. Nó đặt các tiêu đề HTTP cho phản hồi.** 
* **D. Nó phân tích nội dung XML trong thẻ tùy chỉnh.** 

**Trả lời:** B. Nó chỉ định đầu ra của thẻ tùy chỉnh vào trang JSP. 

**Giải thích:** Phương thức `doTag()` trong một `SimpleTagSupport` (thường được sử dụng cho custom tag handlers) là nơi logic chính của thẻ tùy chỉnh được thực thi và nơi nội dung được tạo ra và ghi vào `JspWriter` để xuất ra trang JSP. 

**4. Mục đích của phương thức `contextDestroyed(ServletContextEvent sce)` trong `ServletContextListener` là gì?** 
* **A. Để khởi tạo các servlet trong ứng dụng web.** 
* **B. Để xử lý các ngoại lệ được ném ra trong quá trình khởi tạo servlet.** 
* **C. Để dọn dẹp tài nguyên khi ứng dụng web đang tắt.** 
* **D. Để quản lý việc hết hạn và xóa phiên.** 

**Trả lời:** C. Để dọn dẹp tài nguyên khi ứng dụng web đang tắt. 

**Giải thích:** Phương thức `contextDestroyed()` của `ServletContextListener` được gọi khi ứng dụng web bị hủy (ví dụ, khi máy chủ bị tắt hoặc ứng dụng được triển khai lại). Đây là nơi thích hợp để giải phóng các tài nguyên đã được cấp phát trong `contextInitialized()`, chẳng hạn như đóng kết nối cơ sở dữ liệu hoặc giải phóng bộ nhớ. 

**5. Trong các câu sau, đâu là cú pháp đúng của phương thức được sử dụng để lấy tham số đã khởi tạo trong `ServletContext` hoặc `ServletConfig`?** 
* **A. String getInitializedParameter(String name)** 
* **B. String getInitParameter(String name)** 
* **C. String getContextParameter(String name)** 
* **D. String getBoolParameter(String name)** 

**Trả lời:** B. String getInitParameter(String name) 

**Giải thích:** Cả `ServletContext` và `ServletConfig` đều cung cấp phương thức `getInitParameter(String name)` để truy xuất giá trị của một tham số khởi tạo (initialization parameter) được định nghĩa trong `web.xml` hoặc thông qua chú thích `@WebInitParam`. 

**6. Thuộc tính nào của phần tử `<tag>` được sử dụng để chỉ định tên của thẻ tùy chỉnh (custom tag)?** 
* **A. name** 
* **B. class** 
* **C. body-content** 
* **D. description** 

**Trả lời:** A. name 

**Giải thích:** Trong TLD (Tag Library Descriptor) file, thuộc tính `name` của phần tử `<tag>` được sử dụng để định nghĩa tên của thẻ tùy chỉnh. Tên này sau đó sẽ được sử dụng trong JSP để gọi thẻ, ví dụ: `<myprefix:name>`. 

**7. Làm thế nào một Simple Tag Handler có thể truy cập nội dung phần thân của thẻ tùy chỉnh?** 
* **A. Bằng cách sử dụng phương thức `getWriter()` của lớp `JspWriter`.** 
* **B. Bằng cách triển khai giao diện `BodyTag` trong lớp xử lý thẻ.** 
* **C. Bằng cách sử dụng phương thức `getJspContext().getOut()` của lớp `JspContext`.** 
* **D. Bằng cách sử dụng phương thức `getParent()` của giao diện `javax.servlet.jsp.tagext.Tag`.** 

**Trả lời:** C. Bằng cách sử dụng phương thức `getJspContext().getOut()` của lớp `JspContext`. 

**Giải thích:** `SimpleTagHandler` sử dụng phương thức `getJspBody()` để lấy `JspFragment` đại diện cho phần thân của thẻ. Sau đó, `JspFragment` có thể được gọi với một `Writer` để xử lý và xuất nội dung phần thân. `getJspContext().getOut()` cung cấp `JspWriter` để ghi nội dung ra trang JSP, và thường được dùng kết hợp với `getJspBody().invoke(null)` hoặc `getJspBody().invoke(getJspContext().getOut())` để xử lý body content.

**8. Khi nhiều bộ lọc được áp dụng cho một servlet, điều gì quyết định thứ tự thực thi?** 
* **A. Thứ tự các bộ lọc được định nghĩa trong tệp web.xml.** 
* **B. Thuộc tính ưu tiên của bộ lọc.** 
* **C. Thứ tự các bộ lọc được thêm vào ứng dụng web.** 
* **D. Mẫu URL của servlet.** 

**Trả lời:** A. Thứ tự các bộ lọc được định nghĩa trong tệp web.xml. 

**Giải thích:** Trong các ứng dụng web Java EE, thứ tự thực thi của các bộ lọc được xác định bởi thứ tự chúng được khai báo trong tệp `web.xml` (hoặc thứ tự các chú thích `@WebFilter` được quét, nếu sử dụng cấu hình dựa trên chú thích). 

**9. Đâu KHÔNG phải là một thành phần của kiến trúc MVC trong các framework web Java?** 
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

**10. Phương thức đầu tiên được gọi khi một bộ lọc được khởi tạo trong một ứng dụng web là gì?** 
* **A. initFilter()** 
* **B. initialize()** 
* **C. init()** 
* **D. setupFilter()** 

**Trả lời:** C. init() 

**Giải thích:** Khi một bộ lọc (Filter) được khởi tạo bởi bộ chứa servlet, phương thức `init(FilterConfig filterConfig)` của nó sẽ được gọi đầu tiên. Phương thức này được sử dụng để thực hiện các thao tác khởi tạo một lần cho bộ lọc. 

**11. Kiến trúc MVC là gì?**
* **A. Multi-View Controller**
* **B. Module-View-Controller**
* **C. Model-View-Controller**
* **D. Model-Value-Configuration**

**Trả lời:** C. Model-View-Controller

**Giải thích:** MVC là viết tắt của Model-View-Controller, một mẫu kiến trúc phần mềm được sử dụng rộng rãi để phát triển giao diện người dùng.

**12. Phương thức GET xử lý dữ liệu nhạy cảm như thế nào so với phương thức POST?**
* **A. GET mã hóa dữ liệu đảm bảo truyền tải an toàn.**
* **B. POST phù hợp hơn cho việc truyền dữ liệu an toàn.**
* **C. GET hiển thị dữ liệu nhạy cảm trong URL.**
* **D. GET có thể xử lý lượng dữ liệu lớn hơn POST.**

**Trả lời:** C. GET hiển thị dữ liệu nhạy cảm trong URL.

**Giải thích:** Phương thức GET truyền dữ liệu dưới dạng các tham số trong chuỗi truy vấn của URL, làm cho dữ liệu có thể nhìn thấy được trong lịch sử trình duyệt, nhật ký máy chủ và dễ bị tấn công. Ngược lại, POST gửi dữ liệu trong phần thân của yêu cầu HTTP, an toàn hơn cho dữ liệu nhạy cảm.

**13. Phương thức nào được gọi khi một servlet bị xóa khỏi dịch vụ?**
* **A. destroy()**
* **B. stop()**
* **C. end()**
* **D. dispose()**

**Trả lời:** A. destroy()

**Giải thích:** Phương thức `destroy()` của một servlet được gọi bởi bộ chứa servlet khi servlet đó bị xóa khỏi dịch vụ, thường là khi ứng dụng web bị tắt hoặc hủy triển khai. Đây là nơi để giải phóng bất kỳ tài nguyên nào mà servlet đã giữ.

**14. Mục đích của một bộ lọc ghi nhật ký (logging filter) trong một ứng dụng web Java là gì?**
* **A. Sửa đổi nội dung của phản hồi.**
* **B. Ghi nhật ký các yêu cầu và phản hồi để giám sát.**
* **C. Quản lý thời gian chờ của phiên.**
* **D. Chuyển hướng yêu cầu đến các máy chủ khác.**

**Trả lời:** B. Ghi nhật ký các yêu cầu và phản hồi để giám sát.

**Giải thích:** Một bộ lọc ghi nhật ký (logging filter) được thiết kế để chặn các yêu cầu và phản hồi HTTP, sau đó ghi lại thông tin về chúng (như URL yêu cầu, địa chỉ IP, thời gian phản hồi, v.v.) vào một tệp nhật ký hoặc hệ thống giám sát. Mục đích chính là để theo dõi và gỡ lỗi ứng dụng.

**15. Phương thức `contextInitialized()` của `ServletContextListener` được gọi khi nào?**
* **A. Sau khi máy chủ web nhận được yêu cầu HTTP.**
* **B. Khi một phiên mới được tạo cho một máy khách.**
* **C. Khi ứng dụng web được triển khai hoặc khởi động.**
* **D. Sau khi phản hồi được gửi trở lại máy khách.**

**Trả lời:** C. Khi ứng dụng web được triển khai hoặc khởi động.

**Giải thích:** Phương thức `contextInitialized(ServletContextEvent sce)` của `ServletContextListener` được gọi một lần duy nhất khi ứng dụng web được khởi động thành công (triển khai). Đây là nơi lý tưởng để thực hiện các thao tác khởi tạo toàn cầu cho ứng dụng.

**16. Bạn được giao nhiệm vụ cải thiện hiệu suất của một ứng dụng JSP MVC hiện đang gặp phải thời gian tải trang chậm. Đề xuất một chiến lược để tối ưu hóa ứng dụng, xem xét các nguyên tắc MVC.**
* **A. Tăng dung lượng phần cứng của máy chủ để xử lý nhiều yêu cầu đồng thời hơn.**
* **B. Triển khai cơ chế lưu vào bộ nhớ đệm (caching) trong View để lưu trữ các trang đã được hiển thị.**
* **C. Tối ưu hóa các truy vấn cơ sở dữ liệu trong Model để giảm thời gian truy xuất dữ liệu.**
* **D. Giảm thiểu việc sử dụng kiến trúc MVC và quay lại thiết kế nguyên khối.**

**Trả lời:** C. Tối ưu hóa các truy vấn cơ sở dữ liệu trong Model để giảm thời gian truy xuất dữ liệu.

**Giải thích:** Trong kiến trúc MVC, Model chịu trách nhiệm về dữ liệu và logic nghiệp vụ. Thời gian tải trang chậm thường liên quan đến việc truy xuất dữ liệu kém hiệu quả. Việc tối ưu hóa các truy vấn cơ sở dữ liệu trong Model (ví dụ: tối ưu hóa SQL, sử dụng chỉ mục, giảm số lượng truy vấn) sẽ trực tiếp cải thiện hiệu suất của ứng dụng.

**17. Làm thế nào bạn có thể bao gồm một tệp JSP khác trong một trang JSP?**
* **A. Bằng cách sử dụng thẻ `<import>`.**
* **B. Bằng cách sử dụng chỉ thị `<%@ include %>`.**
* **C. Bằng cách sử dụng thẻ `<link>`.**
* **D. Bằng cách sử dụng thẻ `<external>`.**

**Trả lời:** B. Bằng cách sử dụng chỉ thị `<%@ include %>`.

**Giải thích:** Chỉ thị `<%@ include file="file.jsp" %>` được sử dụng để đưa nội dung của một tệp JSP khác vào trang JSP hiện tại tại thời điểm dịch (translation time). Điều này có nghĩa là nội dung của tệp được đưa vào sẽ được biên dịch cùng với tệp JSP chính.

**18. Làm thế nào bạn có thể tạo một danh sách thả xuống trong một biểu mẫu HTML?**
* **A. Bằng cách sử dụng phần tử `<dropdown>`.**
* **B. Bằng cách sử dụng phần tử `<list>`.**
* **C. Bằng cách sử dụng phần tử `<select>`.**
* **D. Bằng cách sử dụng phần tử `<options>`.**

**Trả lời:** C. Bằng cách sử dụng phần tử `<select>`.

**Giải thích:** Trong HTML, phần tử `<select>` được sử dụng để tạo một danh sách thả xuống. Các tùy chọn trong danh sách được định nghĩa bằng các phần tử `<option>` bên trong thẻ `<select>`.

**19. Các phiên thường được xác định trên phía máy chủ trong phát triển web như thế nào?**
* **A. Địa chỉ IP của máy khách.**
* **B. Chuỗi tác nhân người dùng.**
* **C. ID phiên.**
* **D. Mã thông báo ngẫu nhiên do máy chủ tạo.**

**Trả lời:** C. ID phiên.

**Giải thích:** Các phiên (sessions) trên phía máy chủ thường được xác định bằng một ID phiên (Session ID) duy nhất. ID này được tạo bởi máy chủ và thường được gửi đến máy khách dưới dạng cookie hoặc được thêm vào URL (URL rewriting) để máy khách gửi lại trong các yêu cầu tiếp theo, cho phép máy chủ theo dõi trạng thái của phiên.

**20. Điều nào sau đây là đúng về phương thức HTTP GET?**
* **A. Được máy chủ gọi (thông qua phương thức service) để cho phép servlet xử lý yêu cầu GET.**
* **B. Phương thức GET là phương thức mặc định để truyền thông tin từ trình duyệt đến máy chủ web.**
* **C. Cả hai điều trên đều đúng.**
* **D. Không có điều nào ở trên.**

**Trả lời:** C. Cả hai điều trên đều đúng.

**Giải thích:**
* **A.** Phương thức `doGet()` trong servlet được gọi bởi phương thức `service()` (mà phương thức `service()` lại được gọi bởi bộ chứa servlet) để xử lý các yêu cầu HTTP GET.
* **B.** Khi bạn nhập một URL vào trình duyệt hoặc nhấp vào một liên kết, theo mặc định, trình duyệt sẽ gửi một yêu cầu HTTP GET đến máy chủ web.

**21. Thẻ lõi JSTL nào được sử dụng để xuất giá trị ra trang JSP?**
* **A. `<c:out>`**
* **B. `<c:display>`**
* **C. `<c:print>`**
* **D. `<c:value>`**

**Trả lời:** A. `<c:out>`

**Giải thích:** Thẻ `<c:out>` trong thư viện thẻ lõi JSTL được sử dụng để xuất giá trị của một biểu thức hoặc biến ra trang JSP. Nó cũng cung cấp khả năng thoát (escape) các ký tự đặc biệt của HTML để ngăn chặn các cuộc tấn công XSS.

**22. Đối tượng ngầm định (implicit object) nào cung cấp quyền truy cập vào các tiêu đề HTTP và cookie trong một Java Servlet?**
* **A. request**
* **B. response**
* **C. session**
* **D. application**

**Trả lời:** A. request

**Giải thích:** Đối tượng `HttpServletRequest` (được truy cập thông qua đối tượng ngầm định `request` trong JSP hoặc là tham số `req` trong phương thức `doGet`/`doPost` của servlet) cung cấp các phương thức để truy cập các tiêu đề HTTP (ví dụ: `getHeader()`) và cookie (ví dụ: `getCookies()`) từ yêu cầu của máy khách.

**23. Thứ tự đúng của các giai đoạn vòng đời servlet là gì?**
* **A. Initialization, Service, Destroy**
* **B. Service, Initialization, Destroy**
* **C. Destroy, Service, Initialization**
* **D. Initialization, Destroy, Service**

**Trả lời:** A. Initialization, Service, Destroy

**Giải thích:** Vòng đời của một servlet bao gồm ba giai đoạn chính theo thứ tự:
1.  **Initialization (Khởi tạo):** Phương thức `init()` được gọi một lần khi servlet được khởi tạo.
2.  **Service (Phục vụ):** Phương thức `service()` (hoặc `doGet()`, `doPost()`, v.v.) được gọi cho mỗi yêu cầu đến servlet.
3.  **Destroy (Hủy bỏ):** Phương thức `destroy()` được gọi một lần khi servlet bị xóa khỏi dịch vụ.

**24. Khi nào phương thức `sessionCreated` của `HttpSessionListener` được gọi?**
* **A. Khi người dùng gửi biểu mẫu.**
* **B. Khi một phiên mới được tạo.**
* **C. Khi ngữ cảnh servlet được khởi tạo.**
* **D. Khi một phiên bị hủy bỏ.**

**Trả lời:** B. Khi một phiên mới được tạo.

**Giải thích:** Phương thức `sessionCreated(HttpSessionEvent se)` của `HttpSessionListener` được gọi bởi bộ chứa web ngay sau khi một phiên HTTP mới được tạo ra cho một máy khách.

**25. Trong trang lỗi JSP, làm thế nào bạn có thể truy cập đối tượng ngoại lệ (exception object) được ném ra bởi máy chủ?**
* **A. Bằng cách sử dụng thẻ `<error>`.**
* **B. Bằng cách sử dụng đối tượng ngầm định `exception`.**
* **C. Bằng cách sử dụng đối tượng ngầm định `error`.**
* **D. Bằng cách sử dụng thẻ `<exception>`.**

**Trả lời:** B. Bằng cách sử dụng đối tượng ngầm định `exception`.

**Giải thích:** Khi một trang JSP được chỉ định là trang lỗi (thông qua thuộc tính `errorPage` của trang JSP khác hoặc cấu hình `<error-page>` trong `web.xml`), nó sẽ có quyền truy cập vào đối tượng ngầm định `exception`, đại diện cho ngoại lệ đã được ném ra.

**26. Tệp mô tả triển khai (deployment descriptor) nằm ở đâu?**
* **A. Tệp mô tả triển khai nằm trong thư mục WEB-INF của ứng dụng web.**
* **B. Tệp mô tả triển khai nằm trong thư mục WEB-INFS của ứng dụng web.**
* **C. Tệp mô tả triển khai nằm trong thư mục WEBS-INF của ứng dụng web.**
* **D. Tệp mô tả triển khai nằm trong thư mục WEBS của ứng dụng web.**

**Trả lời:** A. Tệp mô tả triển khai nằm trong thư mục WEB-INF của ứng dụng web.

**Giải thích:** Tệp mô tả triển khai, thường là `web.xml`, phải được đặt trong thư mục `WEB-INF` của ứng dụng web. Thư mục `WEB-INF` là một thư mục đặc biệt không thể truy cập trực tiếp từ máy khách và chứa các tệp cấu hình và lớp Java của ứng dụng.

**27. DBMS xử lý đa người dùng đồng thời như thế nào?**
* **A. Nhóm kết nối (Connection pool) được cung cấp bởi máy chủ DBMS và máy chủ ứng dụng.**
* **B. Sử dụng 1 kết nối được chia sẻ bởi nhiều người dùng.**
* **C. Loại bỏ rò rỉ kết nối trong các ứng dụng cơ sở dữ liệu.**
* **D. Luôn quản lý các tác vụ cơ sở dữ liệu bằng giao dịch.**

**Trả lời:** A. Nhóm kết nối (Connection pool) được cung cấp bởi máy chủ DBMS và máy chủ ứng dụng.

**Giải thích:** Để xử lý đa người dùng đồng thời một cách hiệu quả, hệ quản trị cơ sở dữ liệu (DBMS) và máy chủ ứng dụng thường sử dụng nhóm kết nối (connection pool). Nhóm kết nối duy trì một tập hợp các kết nối cơ sở dữ liệu sẵn sàng để sử dụng, giúp giảm chi phí tạo và đóng kết nối cho mỗi yêu cầu, từ đó cải thiện hiệu suất và khả năng mở rộng.

**28. Trong một Java Servlet, mục đích của phương thức `doPost()` là gì?**
* **A. Xử lý các yêu cầu HTTP GET.**
* **B. Xử lý các yêu cầu HTTP POST.**
* **C. Xử lý các yêu cầu HTTP PUT.**
* **D. Xử lý các yêu cầu HTTP DELETE.**

**Trả lời:** B. Xử lý các yêu cầu HTTP POST.

**Giải thích:** Phương thức `doPost(HttpServletRequest req, HttpServletResponse resp)` trong một Java Servlet được thiết kế đặc biệt để xử lý các yêu cầu HTTP POST được gửi từ máy khách.

**29. Đâu KHÔNG phải là một kiểu JDBC Statement hợp lệ?**
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

**30. Cú pháp nào được sử dụng để biểu thị một biểu thức EL trong trang JSP?**
* **A. ${}**
* **B. #{}**
* **C. @{}**
* **D. %{}**

**Trả lời:** A. ${}

**Giải thích:** Biểu thức ngôn ngữ (Expression Language - EL) trong JSP được bao bọc bởi cú pháp `${}`. Ví dụ: `${user.name}` sẽ truy cập thuộc tính `name` của đối tượng `user`.

**31. Câu lệnh nào sau đây mô tả tốt nhất vai trò của JDBC trong các ứng dụng web?**
* **A. JDBC được sử dụng để tạo các trang web động.**
* **B. JDBC là một giao thức để truyền dữ liệu giữa máy chủ web và trình duyệt.**
* **C. JDBC là một API Java tiêu chuẩn để tương tác với cơ sở dữ liệu.**
* **D. JDBC là một máy chủ web để phục vụ các ứng dụng Java.**

**Trả lời:** C. JDBC là một API Java tiêu chuẩn để tương tác với cơ sở dữ liệu.

**Giải thích:** JDBC (Java Database Connectivity) là một API (Application Programming Interface) của Java, cung cấp một phương tiện tiêu chuẩn để các ứng dụng Java kết nối và tương tác với các cơ sở dữ liệu quan hệ.

**32. Mã trạng thái nào được trả về khi một yêu cầu không thể được thực hiện do cú pháp xấu?**
* **A. 500**
* **B. 400**
* **C. 404**
* **D. 302**

**Trả lời:** B. 400

**Giải thích:** Mã trạng thái HTTP 400 Bad Request cho biết rằng máy chủ không thể xử lý yêu cầu do có lỗi cú pháp không hợp lệ từ phía máy khách.

**33. Phần tử JSP nào KHÔNG được thực thi tại phương thức `service()` của servlet?**
* **A. Scriptlet**
* **B. Expression**
* **C. Declaration**
* **D. Directive**

**Trả lời:** D. Directive

**Giải thích:**
* **Scriptlet (`<% ... %>`)** và **Expression (`<%= ... %>`)** được dịch thành mã Java bên trong phương thức `_jspService()` của servlet được tạo ra từ JSP, và do đó được thực thi khi phương thức `service()` được gọi.
* **Declaration (`<%! ... %>`)** được dịch thành các thành viên (biến hoặc phương thức) của lớp servlet được tạo ra, nằm ngoài phương thức `_jspService()`.
* **Directive (`<%@ ... %>`)** là các chỉ thị được xử lý tại thời điểm dịch (translation time) của JSP, trước khi servlet được biên dịch và do đó không được thực thi bên trong phương thức `service()`.

**34. `ServletContext` trong một ứng dụng web Java là gì?**
* **A. Một đối tượng đại diện cho một thể hiện servlet duy nhất.**
* **B. Một giao diện để tương tác với trình duyệt web của máy khách.**
* **C. Một đối tượng đại diện cho toàn bộ ứng dụng web.**
* **D. Một cơ chế để quản lý dữ liệu phiên.**

**Trả lời:** C. Một đối tượng đại diện cho toàn bộ ứng dụng web.

**Giải thích:** `ServletContext` là một đối tượng duy nhất cho mỗi ứng dụng web được triển khai trên một bộ chứa servlet. Nó cung cấp quyền truy cập vào các tham số khởi tạo cấp ứng dụng, các thuộc tính chung, và cho phép giao tiếp giữa các servlet trong cùng một ứng dụng.

**35. Mục đích của việc sử dụng giao dịch cơ sở dữ liệu trong một ứng dụng web với nhiều thao tác cơ sở dữ liệu là gì?**
* **A. Để đảm bảo tất cả các thao tác được thực hiện đồng thời.**
* **B. Để nhóm các thao tác lại với nhau thành một đơn vị công việc duy nhất.**
* **C. Để tăng khả năng hỏng dữ liệu.**
* **D. Để giảm hiệu suất cơ sở dữ liệu.**

**Trả lời:** B. Để nhóm các thao tác lại với nhau thành một đơn vị công việc duy nhất.

**Giải thích:** Giao dịch cơ sở dữ liệu (database transaction) được sử dụng để nhóm một hoặc nhiều thao tác cơ sở dữ liệu lại với nhau thành một đơn vị công việc logic. Điều này đảm bảo tính toàn vẹn của dữ liệu bằng cách đảm bảo rằng tất cả các thao tác trong giao dịch đều thành công (commit) hoặc tất cả đều thất bại (rollback), tuân theo các thuộc tính ACID.

**36. Tệp nào thường được sử dụng để chỉ định bộ mô tả triển khai và cấu hình cho một ứng dụng web Java?**
* **A. web.config**
* **B. web.xml**
* **C. app.properties**
* **D. deployment.ini**

**Trả lời:** B. web.xml

**Giải thích:** Tệp `web.xml` (Deployment Descriptor) là tệp cấu hình trung tâm cho các ứng dụng web Java EE (Java Servlet). Nó chứa thông tin về các servlet, bộ lọc, trình nghe, ánh xạ URL, tham số khởi tạo, trang lỗi và nhiều cấu hình khác cho ứng dụng web.

**37. Điều nào KHÔNG phải là một kỹ thuật tiêu chuẩn để một phiên bị hủy bỏ chắc chắn?**
* **A. Container bị tắt và khởi động lại.**
* **B. Không có yêu cầu nào đến từ máy khách trong hơn "thời gian chờ phiên" đã cài đặt.**
* **C. Nếu thời gian chờ phiên được đặt thành 0 bằng cách sử dụng phương thức `setMaxInactiveInterval()`.**
* **D. Một servlet gọi rõ ràng `invalidate()` trên một đối tượng phiên.**

**Trả lời:** C. Nếu thời gian chờ phiên được đặt thành 0 bằng cách sử dụng phương thức `setMaxInactiveInterval()`.

**Giải thích:**
* **A.** Khi container bị tắt hoặc khởi động lại, tất cả các phiên sẽ bị hủy bỏ.
* **B.** Nếu không có hoạt động nào từ máy khách trong khoảng thời gian `maxInactiveInterval` (thời gian chờ phiên), phiên sẽ tự động hết hạn.
* **D.** Gọi `session.invalidate()` sẽ hủy bỏ phiên ngay lập tức.
* **C.** Nếu `setMaxInactiveInterval()` được đặt thành 0, phiên sẽ không bao giờ hết hạn tự động; nó chỉ bị hủy bỏ khi trình duyệt đóng hoặc khi `invalidate()` được gọi rõ ràng. Do đó, đây KHÔNG phải là một kỹ thuật để phiên bị hủy bỏ "chắc chắn" trong trường hợp không có hoạt động.

**38. Biểu thức EL `${user.name}` được thực thi trong JSP như thế nào?**
* **A. Nó gọi `user.getName()`**
* **B. Nó truy cập thuộc tính tên của đối tượng người dùng.**
* **C. Nó là một scriptlet.**
* **D. Nó là một khai báo.**

**Trả lời:** B. Nó truy cập thuộc tính tên của đối tượng người dùng.

**Giải thích:** Biểu thức EL `${user.name}` sử dụng cơ chế introspection (phản chiếu) để truy cập thuộc tính `name` của đối tượng `user`. Điều này thường được thực hiện bằng cách tìm kiếm phương thức `getName()` hoặc một trường công khai có tên `name`. EL tự động xử lý việc gọi phương thức getter.

**39. Đâu là cú pháp đúng để truy cập độ dài của một chuỗi được lưu trữ trong thuộc tính yêu cầu có tên "message" bằng cách sử dụng EL?**
* **A. ${message.length}**
* **B. ${requestScope.message.size}**
* **C. ${message.length()}**
* **D. ${fn:length(message)}**

**Trả lời:** D. ${fn:length(message)}

**Giải thích:** Để lấy độ dài của một chuỗi trong EL, bạn cần sử dụng hàm `length()` từ thư viện hàm JSTL (thường được tiền tố là `fn`). Cú pháp đúng là `${fn:length(message)}`.

**40. Mục đích của thuộc tính `pattern` trong thẻ `<fmt:formatNumber>` là gì?**
* **A. Để chỉ định ngôn ngữ của số được định dạng.**
* **B. Để xác định mẫu định dạng số.**
* **C. Để đặt ký hiệu tiền tệ.**
* **D. Để đặt múi giờ cho định dạng.**

**Trả lời:** B. Để xác định mẫu định dạng số.

**Giải thích:** Thuộc tính `pattern` trong thẻ `<fmt:formatNumber>` của JSTL được sử dụng để cung cấp một chuỗi mẫu định dạng số (ví dụ: "###,##0.00" cho định dạng số có dấu phẩy và hai chữ số thập phân).

**41. URL rewriting trong ngữ cảnh ứng dụng web là gì?**
* **A. Một kỹ thuật để che giấu URL nhằm ngăn chặn truy cập trái phép.**
* **B. Một phương pháp chuyển hướng người dùng đến các trang web khác nhau.**
* **C. Một cơ chế để thêm thông tin phiên vào URL.**
* **D. Một quá trình nén URL để cải thiện hiệu suất trang web.**

**Trả lời:** C. Một cơ chế để thêm thông tin phiên vào URL.

**Giải thích:** URL rewriting là một kỹ thuật trong đó một ID phiên (Session ID) được thêm vào URL khi cookie bị vô hiệu hóa hoặc không được hỗ trợ bởi trình duyệt. Điều này cho phép máy chủ theo dõi phiên của người dùng bằng cách truyền ID phiên trong chính URL cho mỗi yêu cầu.

**42. Cấu trúc của Dòng Trạng thái (Status Line) trong Thông báo Phản hồi HTTP là gì?**
* **A. [HTTP Version] [Response Code] [Status]**
* **B. [HTTP Method] [Protocol Version] [Requested Resource forming URI]**
* **C. [HTTP Version] [Response Code] [Http Method]**
* **D. [HTTP Version] [Protocol Code] [Http Method]**

**Trả lời:** A. [HTTP Version] [Response Code] [Status]

**Giải thích:** Dòng trạng thái (Status Line) của một phản hồi HTTP có cấu trúc: `HTTP-Version Status-Code Reason-Phrase`. Trong các lựa chọn, "[HTTP Version] [Response Code] [Status]" là cách diễn giải gần nhất với cấu trúc chuẩn, trong đó "Status" tương ứng với `Reason-Phrase`.

**43. Câu lệnh Java nào mà thẻ `<c:when>` bên trong `<c:choose>` tương tự?**
* **A. if**
* **B. while**
* **C. for**
* **D. switch-case**

**Trả lời:** D. switch-case

**Giải thích:** Các thẻ `<c:choose>`, `<c:when>`, và `<c:otherwise>` trong JSTL hoạt động tương tự như một cấu trúc `switch-case` trong Java. Thẻ `<c:choose>` bắt đầu khối, mỗi thẻ `<c:when>` đại diện cho một trường hợp (`case`), và thẻ `<c:otherwise>` là trường hợp mặc định (`default`).

**44. Phần tử `<rtexprvalue>` chỉ định điều gì trong TLD?**
* **A. Kiểu trả về của lớp xử lý thẻ tùy chỉnh tại thời gian chạy.**
* **B. Liệu thuộc tính có thể chấp nhận các biểu thức thời gian chạy hay không.**
* **C. Kiểu nội dung phần thân của thẻ tùy chỉnh.**
* **D. Lớp xử lý thẻ.**

**Trả lời:** B. Liệu thuộc tính có thể chấp nhận các biểu thức thời gian chạy hay không.

**Giải thích:** Trong tệp mô tả thư viện thẻ (Tag Library Descriptor - TLD), phần tử `<rtexprvalue>` (runtime expression value) trong định nghĩa `<attribute>` được sử dụng để chỉ định xem thuộc tính của thẻ tùy chỉnh có thể chấp nhận một biểu thức kịch bản (scriptlet expression) hoặc biểu thức EL (Expression Language) tại thời gian chạy hay không. Nếu là `true`, bạn có thể truyền các giá trị động cho thuộc tính đó.

**45. Đâu KHÔNG phải là một mục đích sử dụng của bộ lọc trong JSP?**
* **A. Xác thực chặn yêu cầu dựa trên danh tính người dùng.**
* **B. Ghi nhật ký và kiểm toán - Theo dõi việc sử dụng ứng dụng web.**
* **C. Chuyển đổi hình ảnh - Thay đổi kích thước bản đồ, v.v.**
* **D. Liên kết đến tệp bootstrap.min.css trong tệp JSP.**
* **E. Nén dữ liệu - Làm cho các tệp tải xuống nhỏ hơn.**

**Trả lời:** D. Liên kết đến tệp bootstrap.min.css trong tệp JSP.

**Giải thích:** Bộ lọc (Filter) trong các ứng dụng web Java được sử dụng để chặn và xử lý các yêu cầu và phản hồi HTTP trước khi chúng đến servlet hoặc sau khi chúng rời khỏi servlet. Các mục đích sử dụng phổ biến bao gồm:
* Xác thực (Authentication) và ủy quyền (Authorization) 
* Ghi nhật ký (Logging) và kiểm toán (Auditing) 
* Chuyển đổi dữ liệu, bao gồm cả nén hoặc chuyển đổi định dạng
Việc liên kết đến tệp CSS (như `bootstrap.min.css`) là một nhiệm vụ của JSP hoặc HTML, không phải là chức năng của bộ lọc.

**46. Đâu KHÔNG phải là một mục đích sử dụng của bộ lọc trong JSP?**
* **A. Xác thực chặn yêu cầu dựa trên danh tính người dùng.**
* **B. Ghi nhật ký và kiểm toán - Theo dõi việc sử dụng ứng dụng web.**
* **C. Chuyển đổi hình ảnh - Thay đổi kích thước bản đồ, v.v.**
* **D. Liên kết đến tệp bootstrap.min.css trong tệp JSP.**
* **E. Nén dữ liệu - Làm cho các tệp tải xuống nhỏ hơn.**

**Trả lời:** D. Liên kết đến tệp bootstrap.min.css trong tệp JSP.

**Giải thích:** Câu hỏi này lặp lại câu hỏi trước. Bộ lọc (Filter) trong các ứng dụng web Java được sử dụng để chặn và xử lý các yêu cầu và phản hồi HTTP trước khi chúng đến servlet hoặc sau khi chúng rời khỏi servlet. Các mục đích sử dụng phổ biến bao gồm:
* Xác thực (Authentication) và ủy quyền (Authorization) 
* Ghi nhật ký (Logging) và kiểm toán (Auditing) 
* Chuyển đổi dữ liệu, bao gồm cả nén hoặc chuyển đổi định dạng 
Việc liên kết đến tệp CSS (như `bootstrap.min.css`) là một nhiệm vụ của JSP hoặc HTML, không phải là chức năng của bộ lọc.

**47. Trong mô hình dữ liệu đa tầng, tầng nào chịu trách nhiệm xử lý logic ứng dụng?**
* **A. Tầng giao diện người dùng/ứng dụng.**
* **B. Tầng logic ứng dụng.**
* **C. Tầng dữ liệu.**
* **D. Tầng kết nối.**

**Trả lời:** B. Tầng logic ứng dụng.

**Giải thích:** Trong kiến trúc đa tầng (multi-tier architecture), tầng logic ứng dụng (Application Logic Layer), còn được gọi là tầng nghiệp vụ (Business Layer), chịu trách nhiệm chứa và thực thi các quy tắc nghiệp vụ, logic xử lý và các phép tính chính của ứng dụng.

**48. Trong một ứng dụng web Java tiêu chuẩn, tệp mô tả triển khai (web.xml) thường nằm ở đâu?**
* **A. WEB-INF**
* **B. META-INF**
* **C. WEB-INF/classes**
* **D. Thư mục gốc**

**Trả lời:** A. WEB-INF

**Giải thích:** Tệp `web.xml`, là tệp mô tả triển khai của ứng dụng web Java, luôn được đặt trong thư mục `WEB-INF` của cấu trúc thư mục ứng dụng web.

**49. Trong quá trình gọi phương thức nào của JSP, dữ liệu biểu mẫu và cookie có sẵn?**
* **A. jspInit()**
* **B. _jspService()**
* **C. jspDestroy()**
* **D. jspDoStart()**

**Trả lời:** B. _jspService()

**Giải thích:** Phương thức `_jspService()` là phương thức chính được tạo ra bởi bộ chứa servlet từ một JSP. Phương thức này tương ứng với phương thức `service()` của một servlet thông thường và là nơi các yêu cầu được xử lý. Do đó, các đối tượng `request` và `response` (bao gồm dữ liệu biểu mẫu và cookie) có sẵn trong phương thức này.

**50. Một trình nghe phiên (session listener) làm gì trong một ứng dụng web?**
* **A. Nó lắng nghe và ghi lại các cuộc hội thoại.**
* **B. Nó theo dõi các thay đổi trong phiên người dùng, giống như khi ai đó đăng nhập hoặc đăng xuất.**
* **C. Nó thay đổi dữ liệu phiên.**
* **D. Nó giúp người dùng điều hướng ứng dụng.**

**Trả lời:** B. Nó theo dõi các thay đổi trong phiên người dùng, giống như khi ai đó đăng nhập hoặc đăng xuất.

**Giải thích:** Một trình nghe phiên (session listener), cụ thể là `HttpSessionListener`, được sử dụng để theo dõi các sự kiện trong vòng đời của phiên HTTP, chẳng hạn như khi một phiên được tạo (`sessionCreated`) hoặc bị hủy bỏ (`sessionDestroyed`). Điều này hữu ích cho việc quản lý tài nguyên hoặc ghi nhật ký các hoạt động liên quan đến phiên.

**51. Cú pháp nào EL sử dụng để truy cập một phần tử trong một danh sách?**
* **A. ${list[index]}**
* **B. ${list.get(index)}**
* **C. ${list(index)}**
* **D. ${list.element[index]}**

**Trả lời:** A. ${list[index]}

**Giải thích:** Trong Expression Language (EL), bạn có thể truy cập các phần tử của một `List` hoặc mảng bằng cách sử dụng toán tử dấu ngoặc vuông `[]` với chỉ số. Ví dụ: `${list[0]}` sẽ truy cập phần tử đầu tiên của danh sách.