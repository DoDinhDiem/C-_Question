### Câu hỏi cơ bản về CSDL:

1. **Cơ sở dữ liệu là gì?**

   - **Trả lời:** Cơ sở dữ liệu (CSDL) là một tập hợp các dữ liệu có tổ chức được lưu trữ và quản lý trong máy tính, thường được tổ chức theo một mô hình dữ liệu cụ thể và được truy cập bằng các truy vấn.

2. **Sự khác biệt giữa CSDL quan hệ và CSDL phi quan hệ là gì?**

   - **Trả lời:**
     - **CSDL quan hệ:** Dữ liệu được tổ chức trong các bảng mà mỗi bảng có các hàng và cột. Các quan hệ giữa các bảng được xác định bằng các khóa ngoại.
     - **CSDL phi quan hệ:** Dữ liệu không được tổ chức theo cấu trúc bảng, thay vào đó dùng các cấu trúc dữ liệu phức tạp hơn như tài liệu, đồ thị hoặc cặp khóa giá trị.

3. **SQL là gì?**

   - **Trả lời:** SQL (Structured Query Language) là một ngôn ngữ lập trình được sử dụng để truy cập và quản lý dữ liệu trong cơ sở dữ liệu quan hệ. SQL bao gồm các câu lệnh như SELECT, INSERT, UPDATE, DELETE để thao tác với dữ liệu.

4. **Sự khác biệt giữa DDL, DML, và DCL là gì?**

   - **Trả lời:**
     - **DDL (Data Definition Language):** Dùng để định nghĩa cấu trúc dữ liệu như tạo bảng, xóa bảng, thay đổi cấu trúc bảng.
     - **DML (Data Manipulation Language):** Dùng để thao tác với dữ liệu như thêm, sửa, xóa dữ liệu từ bảng.
     - **DCL (Data Control Language):** Dùng để quản lý quyền truy cập và an ninh dữ liệu như GRANT, REVOKE.

5. **Khái niệm Primary Key là gì?**
   - **Trả lời:** Primary Key là một cột hoặc một tập hợp các cột trong bảng được sử dụng để duy nhất xác định mỗi hàng trong bảng. Giá trị của Primary Key phải là duy nhất và không thể null.

### Câu hỏi nâng cao về CSDL:

1. **Sự khác biệt giữa Inner Join và Outer Join là gì?**

   - **Trả lời:**
     - **Inner Join:** Trả về các bản ghi từ cả hai bảng mà có điều kiện kết nối giữa chúng đúng.
     - **Outer Join:** Trả về tất cả các bản ghi từ ít nhất một bảng kể cả khi điều kiện kết nối không đúng. Có ba loại Outer Join: LEFT OUTER JOIN, RIGHT OUTER JOIN và FULL OUTER JOIN.

2. **Normalization là gì và tại sao nó quan trọng trong CSDL?**

   - **Trả lời:** Normalization là quá trình thiết kế cơ sở dữ liệu để giảm thiểu sự lặp lại dữ liệu và đảm bảo tính nhất quán. Nó quan trọng vì:
     - Giảm thiểu lãng phí dữ liệu.
     - Đảm bảo tính nhất quán và cập nhật dễ dàng.
     - Tăng hiệu suất và giảm dung lượng lưu trữ.

3. **Index là gì và tại sao nó quan trọng?**
   - **Trả lời:** Index là một cấu trúc dữ liệu phụ được sử dụng để tăng tốc độ truy xuất dữ liệu từ cơ sở dữ liệu. Index quan trọng vì:
     - Tăng tốc độ truy xuất dữ liệu.
     - Hỗ trợ việc tìm kiếm và sắp xếp dữ liệu.
     - Giảm tải cho hệ thống cơ sở dữ liệu

### Câu hỏi về Thủ tục (Stored Procedures):

1. **Thủ tục lưu trữ (Stored Procedure) là gì?**

   - **Trả lời:** Thủ tục lưu trữ là một tập hợp các câu lệnh SQL được lưu trữ trên máy chủ cơ sở dữ liệu và có thể được gọi bởi các ứng dụng hoặc các thủ tục khác. Thủ tục lưu trữ thường được sử dụng để thực hiện các tác vụ phức tạp, xử lý dữ liệu và thực hiện logic kinh doanh trong cơ sở dữ liệu.

2. **Lợi ích của việc sử dụng thủ tục lưu trữ là gì?**

   - **Trả lời:**
     - Tăng hiệu suất: Thủ tục lưu trữ thường được biên dịch và lưu trữ trên máy chủ, giúp giảm bớt lưu lượng mạng và tăng tốc độ xử lý.
     - Bảo mật: Ngăn chặn truy cập trực tiếp vào dữ liệu bằng cách cung cấp quyền truy cập chỉ vào thủ tục thay vì các bảng.
     - Tính nhất quán: Đảm bảo rằng các hành động được thực hiện trên dữ liệu luôn nhất quán và tuân theo các quy tắc kinh doanh được xác định trước.

3. **Cách tạo và gọi thủ tục lưu trữ trong SQL Server là gì?**

   - **Trả lời:**
     - **Tạo thủ tục lưu trữ:**
       ```sql
       CREATE PROCEDURE sp_GetEmployee
       AS
       BEGIN
           SELECT * FROM Employees;
       END
       ```
     - **Gọi thủ tục lưu trữ:**
       ```sql
       EXEC sp_GetEmployee;
       ```

4. **Có thể truyền tham số vào thủ tục lưu trữ không? Nếu có, cách làm như thế nào?**

   - **Trả lời:** Có, bạn có thể truyền tham số vào thủ tục lưu trữ. Để làm điều này, bạn cần chỉ định các tham số trong khai báo của thủ tục và sử dụng chúng trong câu lệnh SQL bên trong thủ tục.

   ```sql
   CREATE PROCEDURE sp_GetEmployeeByID
   @EmployeeID INT
   AS
   BEGIN
       SELECT * FROM Employees WHERE EmployeeID = @EmployeeID;
   END
   ```

5. **Làm thế nào để trả về giá trị từ một thủ tục lưu trữ?**
   - **Trả lời:** Bạn có thể sử dụng câu lệnh `RETURN` để trả về một giá trị từ một thủ tục lưu trữ. Ngoài ra, bạn cũng có thể sử dụng tham số OUTPUT để trả về giá trị.
   ```sql
   CREATE PROCEDURE sp_GetEmployeeCount
   @Count INT OUTPUT
   AS
   BEGIN
       SELECT @Count = COUNT(*) FROM Employees;
   END
   ```

### Câu hỏi về Hàm (Functions):

1. **Hàm trong cơ sở dữ liệu là gì?**

   - **Trả lời:** Hàm trong cơ sở dữ liệu là một khối lệnh có thể được gọi từ các truy vấn hoặc thủ tục lưu trữ. Hàm thường thực hiện một công việc cụ thể và trả về một giá trị.

2. **Sự khác biệt giữa hàm và thủ tục lưu trữ là gì?**

   - **Trả lời:**
     - **Thủ tục lưu trữ:** Thực hiện các tác vụ xử lý dữ liệu và thường không trả về kết quả.
     - **Hàm:** Thực hiện một công việc cụ thể và trả về một giá trị. Hàm có thể được sử dụng trong câu lệnh SELECT hoặc từ các thủ tục lưu trữ.

3. **Có thể sử dụng hàm tích hợp sẵn trong cơ sở dữ liệu không?**

   - **Trả lời:** Có, hầu hết các hệ quản trị cơ sở dữ liệu cung cấp các hàm tích hợp sẵn cho các nhiệm vụ phổ biến như chuỗi, ngày tháng, toán học, và biến đổi dữ liệu.

4. **Cách tạo và gọi một hàm trong SQL Server là gì?**

   - **Trả lời:**
     - **Tạo hàm:**
       ```sql
       CREATE FUNCTION fn_GetEmployeeCount()
       RETURNS INT
       AS
       BEGIN
           DECLARE @Count INT;
           SELECT @Count = COUNT(*) FROM Employees;
           RETURN @Count;
       END
       ```
     - **Gọi hàm:**
       ```sql
       SELECT dbo.fn_GetEmployeeCount();
       ```

5. **Có thể truyền tham số vào hàm không? Nếu có, cách làm như thế nào?**
   - **Trả lời:** Có, bạn có thể truyền tham số vào hàm. Tương tự như thủ tục lưu trữ, bạn cần chỉ định các tham số trong khai báo của hàm

Dưới đây là một số câu hỏi và câu trả lời liên quan đến trigger trong cơ sở dữ liệu:

### Câu hỏi về Trigger:

1. **Trigger trong cơ sở dữ liệu là gì?**

   - **Trả lời:** Trigger là một loại đối tượng trong cơ sở dữ liệu được kích hoạt tự động khi có một sự kiện xảy ra trên bảng hoặc view. Trigger thường được sử dụng để thực hiện các hành động như kiểm tra và thay đổi dữ liệu sau khi xảy ra một sự kiện như INSERT, UPDATE hoặc DELETE.

2. **Sự khác biệt giữa trigger "BEFORE" và "AFTER" là gì?**

   - **Trả lời:**
     - **BEFORE Trigger:** Kích hoạt trước khi hành động DML (INSERT, UPDATE, DELETE) được thực hiện trên bảng.
     - **AFTER Trigger:** Kích hoạt sau khi hành động DML đã được thực hiện trên bảng.

3. **Khi nào bạn nên sử dụng trigger?**

   - **Trả lời:** Trigger thường được sử dụng khi cần thực hiện các hành động tự động sau khi xảy ra các sự kiện trên bảng như INSERT, UPDATE, hoặc DELETE. Một số trường hợp sử dụng trigger bao gồm:
     - Kiểm tra và bảo đảm tính nhất quán dữ liệu.
     - Ghi log hoạt động.
     - Thay đổi dữ liệu hoặc thực hiện các hành động phức tạp dựa trên các sự kiện.

4. **Có bao nhiêu loại trigger trong cơ sở dữ liệu?**

   - **Trả lời:** Có hai loại trigger chính trong cơ sở dữ liệu:
     - **Row-level Trigger:** Kích hoạt mỗi khi một hàng dữ liệu trong bảng được ảnh hưởng bởi một hành động DML.
     - **Statement-level Trigger:** Kích hoạt một lần cho mỗi lệnh DML thực hiện trên bảng, bất kể số lượng hàng bị ảnh hưởng.

5. **Các sự kiện trigger phổ biến là gì?**
   - **Trả lời:** Các sự kiện trigger phổ biến bao gồm:
     - INSERT: Kích hoạt sau khi một hoặc nhiều hàng được chèn vào bảng.
     - UPDATE: Kích hoạt sau khi một hoặc nhiều hàng trong bảng được cập nhật.
     - DELETE: Kích hoạt sau khi một hoặc nhiều hàng được xóa khỏi bảng.

### Câu hỏi nâng cao về Trigger:

1. **Sự khác biệt giữa trigger "FOR EACH ROW" và "FOR EACH STATEMENT" là gì?**

   - **Trả lời:**
     - **FOR EACH ROW:** Trigger kích hoạt một lần cho mỗi hàng dữ liệu bị ảnh hưởng bởi lệnh DML.
     - **FOR EACH STATEMENT:** Trigger kích hoạt một lần cho mỗi lệnh DML, bất kể số lượng hàng bị ảnh hưởng.

2. **Có thể sử dụng trigger trong trường hợp nào không nên?**

   - **Trả lời:** Mặc dù trigger có thể hữu ích, nhưng cũng cần cân nhắc về hiệu suất và tính bảo trì. Trigger nên tránh sử dụng trong các tình huống sau:
     - Khi gây ra tác động đến hiệu suất của hệ thống do các hành động phức tạp hoặc đợi lâu.
     - Khi gây ra sự rối loạn trong logic xử lý do sự phụ thuộc vào các hành động tự động không rõ ràng.

3. **Làm thế nào để kiểm tra và xóa trigger từ cơ sở dữ liệu?**

   - **Trả lời:** Để kiểm tra trigger có sẵn trong cơ sở dữ liệu, bạn có thể sử dụng câu lệnh `SHOW TRIGGERS` hoặc truy vấn các bảng hệ thống như `information_schema.triggers`. Để xóa trigger, bạn có thể sử dụng câu lệnh `DROP TRIGGER`.

   ```sql
   SHOW TRIGGERS;
   DROP TRIGGER IF EXISTS trigger_name;
   ```

4. **Có thể sử dụng nested trigger trong cơ sở dữ liệu không?**

   - **Trả lời:** Có, nhưng cần cẩn thận. Nested trigger là trigger được kích hoạt bởi một hành động của trigger khác. Sử dụng nested trigger có thể gây ra các vấn đề về hiệu suất và logic xử lý phức tạp. Do đó, nên cân nhắc và kiểm soát việc sử dụng nested trigger.

5. **Có cách nào để bảo vệ các trigger khỏi việc gây ra vấn đề về hiệu suất không?**
   - **Trả lời:** Để bảo vệ các trigger khỏi việc gây ra vấn đề về hiệu suất, bạn có thể:
     - Đảm bảo rằng trigger được tối ưu hóa và thực hiện ít công việc phức tạp nhất có thể.
     - Kiểm tra và
