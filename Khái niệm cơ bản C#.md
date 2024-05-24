### **1. C# là gì**

- `C#` là ngôn ngữ lập trình đơn giản được phát triển bởi đội ngũ Microsoft vào năm 2000
- `C#` là ngôn ngữ lập trình hiện đại hiện đại, hướng đối tượng và nó được xây dựng trên nền tảng của hai ngôn ngữ mạnh nhất C++ và java
- `C#` với sự hỗ trợ mạnh mẽ của .Net Framework giúp cho việc tạo ứng dựng Windows Forms hay WPF,.. trở nên dễ dàng.

### **2. Đặc trưng của C#**

**C# là ngôn ngữ đơn giản**

- `C#` dựa trên nền tảng của C++ và java nên ngôn ngữ C# khá đơn giản.
- Nó đã được cải tiến để làm cho ngôn ngữ đơn giản hơn. Một vài trong các sự cải tiến là loại bỏ các dư thừa, hay thêm vào những cú pháp thay đổi.

**C# là ngôn ngữ hiện đại**

- Một vài khái niệm mới mẻ khá mơ hồ với các bạn mới như xử lý loại lệ, những kiểu dữ liệu mở rộng, bảo mật mã nguồn. Đây là những đặc tính hiện đại cần có. và `C#` chứa tất cả các đặc tính nêu trên

**C# là ngôn ngữ lập trình hướng đối tượng**

- Lập tình hướng đối tượng là một phương pháp lập trình có 4 tính chất.Đó là:
  - Tình trừu tượng(abstraction)
  - Tính đóng gói(encapsulation)
  - Tính đa hình(polymorphism)
  - Tính kế thừa(inheritance)

**C# là ngôn ngữ ít từ khóa**

- `C#` được mô tả là ngôn ngữ sử dụng giới hạn những từ khóa (gồm khoảng 80 từ khóa và mười mấy kiểu dữ liệu xây dựng sẵn).

### **3. List trong C#**

#### **3.1 List trong C# là gì?**

- List trong `C#` được sử dụng để lưu trữ và quản lý một danh sách là tập hợp các đối tượng theo kiểu mảng. Nó có thể truy cập bằng chỉ mục và có các phương pháp sắp xếp, tìm kiếm và sửa dổi danh sách
  ![List](https://freetuts.net/upload/tut_post/images/2021/02/02/3557/list-01.jpg)
  **Các đặc điểm của List:**
  - List tương đương với ArayList.
  - Thuộc System.collection.Generic namepace
  - Có thể chứa các dữ liệu thuộc kiểu dữ liệu chỉ định.
  - Các phần tử có thể thêm bằng phương thức Add(), AddRange() hoặc bằng phương thức khởi tạo.
  - Các phần tử được truy cập bằng chỉ mục(List[0])
  - List hoạt động nhanh hơn và it lỗi hơn ArayList.

#### **3.2 Các thuộc tính và phương thức của list**

**Các thuộc tính của List:**
| Thuộc tính | Mô tả |
|:-----------|:------|
| Items | Nhận hoặc đặt phần tử ở chỉ mục được chỉ định |
| Count | Trả về tổng số phần tử trong List |

**Các phương thức của List:**
| Phương pháp | Mô tả |
|:------------|:------|
| Add() | Thêm một phần tử vào cuối danh sách |
| AddRange() | Thêm các phần tử được chỉ định vào cuối danh sách |
| BinarySearch | Tìm kiếm phần tử và trả về một chỉ mục của phần tử |
| Clear() | Loại bỏ tất cả các phần tử khỏi Danh sách <T>. |
| Contains() | Kiểm tra xem phần tử được chỉ định có tồn tại hay không trong Danh sách <T>. |
| Find() | Tìm phần tử đầu tiên được chỉ định.|
| Foreach() | Lặp lại qua một danh sách <T>. |
| Insert() | Chèn một phần tử tại chỉ mục được chỉ định trong Danh sách <T>. |
| InsertRange() | Chèn các phần tử của một tập hợp khác vào chỉ mục được chỉ định. |
| Remove() | Loại bỏ sự xuất hiện đầu tiên của phần tử được chỉ định. |
| RemoveAt() | Loại bỏ phần tử tại chỉ mục được chỉ định. |
| RemoveRange() | Loại bỏ tất cả các phần tử. |
| Sort() | Sắp xếp tất cả các phần tử. |
| TrimExcess() | Đặt dung lượng thành số phần tử thực tế. |
| TrueForAll | Xác định xem mọi phần tử trong Danh sách <T> có khớp với các điều kiện được xác định bởi vị từ được chỉ định hay không. |

#### **3.3 Các thao tác với List**

**Tạo List**
Để tạo một list ta sử dụng từ khóa new cùng với đó là kiểu dữ liệu cho tham số cần lưu trữ

```
List<int> primeNumbers = new List<int>();
//thêm phần bằng phương thức Add
primeNumbers.Add(1);
primeNumbers.Add(3);
primeNumbers.Add(5);
primeNumbers.Add(7);

var cities = new List<string>();
cities.Add("New York");
cities.Add("London");
cities.Add("Mumbai");
cities.Add("Chicago");
cities.Add(null);

//thêm phần tử bằng cách khởi tạo
var bigCities = new List<string>()
{
  "New York",
  "London",
  "Mumbai",
  "Chicago"
};
var students = new List<Student>() {
  new Student(){ Id = 1, Name="Nam"},
  new Student(){ Id = 2, Name="Phong"},
  new Student(){ Id = 3, Name="Quyền"},
  new Student(){ Id = 4, Name="Tiến"}
};
```

Để thêm tất cả các phần tử từ một array hoặc một list khác ta sử dụng AddRange()

```
IList<int> intList1 = new List<int>();
//sử dụng phương thức add() để thêm phần tử
intList1.Add(10);
intList1.Add(20);
intList1.Add(30);
intList1.Add(40);
//tạo một List mới
List<int> intList2 = new List<int>();
//thêm phần tử của intList1 vào intList2
intList2.AddRange(intList1);
```

**Truy cập List**
Danh sách có thể được truy cập bằng chỉ mục(index), vòng lặp for/foreach và sử dụng câu truy vấn LINQ. Các chỉ mục của danh sách bắt đầu từ số 0 và đặt trong dâu hoặc ngoặc vuông.

```
//khai báo và khởi tạo phần tử cho intList
List<int> intList = new List<int>() { 10, 20, 30, 40, 50 };
//sử dụng foreach để truy xuất toàn bộ phần tử
intList.ForEach(el => Console.WriteLine(el));
foreach (var el in intList)
  Console.WriteLine(el);
//sử dụng for để truy xuất phần tử
for(int i =0; i < intList.Count; i++)
  Console.WriteLine(intList[i]);
```

**Truy cập List bằng LINQ**
Chúng ta có thể truy cập vào danh sách bằng cách sử dụng cú pháp truy vấn LINQ hoặc cú pháp phương thức dưới đây:

```
var students = new List<Student>() {
  new Student(){ Id = 1, Name="Nam" },
  new Student(){ Id = 2, Name="Phong" },
  new Student(){ Id = 3, Name="Quyền" },
  new Student(){ Id = 4, Name="Tiến" },
  new Student(){ Id = 5, Name="Nam" }
};
//lấy tất cả học sinh có tên Nam
var studNames = from s in students
where s.Name == "Nam"
select s;
```

**Chèn phần tử vào List**
Sử dụng phương thức Insert() để chèn phần tử vào vị trí index được chỉ định.

- Cú pháp

```
void Insert(int index, T item);
```

- Ví dụ

```
var numbers = new List<int>(){ 10, 20, 30, 40 };
// chèn phần tử 11 vào vị trí 1
numbers.Insert(1, 11);
//->> {10, 11, 20, 30, 40}
```

**Xóa phần tử khỏi List**
Sử dụng phương thức Remove() để xóa phần tử xuất hiện đầu tiên trong List. Hoặc sử dụng phương thức RemoveAt() để xóa phần tử tại một vị trí index chỉ định.

- Cú pháp

```
bool Remove(T item)
void RemoveAt(int index)
```

- Ví dụ

```
var numbers = new List<int>(){ 10, 20, 30, 40, 10 };
//xóa phần tử 10 trong danh sách
numbers.Remove(10);
//xóa phần tử thứ 2 trong danh sách
numbers.RemoveAt(2);
```

**Kiểm tra phần tử trong List **
Sử dụng phương thức `Contains` để kiểm tra xem một phần tử có tồn tại trong List hay không. Nếu tồn tại trả về true nếu không thì trả về false.

Ví dụ:

```
var numbers = new List<int>(){ 10, 20, 30, 40 };
numbers.Contains(10); // returns true
numbers.Contains(11); // returns false
numbers.Contains(20); // returns true
```

### **4. Kiểu dữ liệu**

#### **Kiểu tham chiếu**

**Kiểu object**

- Đây là kiểu dữ liệu cơ bản nhất của tất cả các kiểu dữ liệu trong .Net. Mọi kiểu dữ liệu đều được kế thừa từ System.Object nên kiểu object có thể gán mọi giá trị của các kiểu dữ liệu khác như tam chiếu, kiểu giá trị hoặc kiểu do người dùng tự định nghĩa

```
object obj;
obj = 123;
 // chúng ta đã chuyển kiểu dữ liệu object sang kiểu giá trị.
```

**Kiểu dynamic**

- Đây là kiểu dữ liệu mới được đưa vào trong `C#` 4.0. Ta có lưu mọi kiểu giá trị trong biến kiểu dynamic. Đối tượng thuộc kiểu này sẽ không xác định được kiểu dữ liệu cho đến khi chương trình được thực thi

```
dynamic <tên biến>;
//hoặc
dynamic <tên biến> = <giá trị>;
```

#### **Kiểu con trỏ**

Biến kiểu con trỏ lưu địa chỉ bộ nhớ của kiểu khác. con trỏ trong `C#` có cùng khả năng như con trỏ trong C hoặc C++. Cú pháp để khai báo biến kiểu con trỏ là: `type*identifier`

```
char*abc;
int*xyz;
```

### **5. Lớp và đối tượng trong C#**

#### **5.1 Đối tượng**

- Đối tượng (object) là một thực thể trong thế giới thực ví dụ như cái bàn, cây viết, điện thoại,..
- Đổi tượng là 1 thực thể có trạng thái(dữ liệu) và hành vi(phương thức).
- Đối tượng là 1 thực thể runtime vì nó được đạo ra trong thời gian chương trình chạy. Đối tượng là thể hiện của một lớp. Tất cả các thành viên của lớp có thể được truy cập thông qua đối tượng.
- Để tạo đối tượng chúng ta sử dụng từ khóa `new`

```
People p1 = new People();
```

#### **5.2 Lớp**

- Trong `C#` lớp (class) là một nhóm các đối tượng tương tự nhau. Nó là một khuôn mẫu mà từ đó các đối tượng được tạo ra. Nó có thể có các trường, phương thức, hàm xây dựng, hàm hủy
- Ví dụ sau có lớp con người có trạng thái là tên, tuổi cmnd và có hành vi nói viết

```
public class People
 {
     string name;
     int old;
     string Id;
     private void speak() {};
     private void write() {};
 }
```

#### **5.3 Ví dụ**

```
using System;

namespace ConsoleApp3
{
    public class People
    {
        public int id;
        public String name;
        public int old;
        public People(int id, String name, int old)
        {
            this.id = id;
            this.name = name;
            this.old = old;
        }
        public void Show()
        {
            Console.WriteLine("Id = " + id + ", Name = " + name + ", old = " + old);
        }
    }
    class Test
    {
        public static void Main(string[] args)
        {
            People p1 = new People(12, "Nguyen Van A", 20);
            People p2 = new People(18, "Nguyen Van B", 21);
            p1.Show();
            p2.Show();
            Console.ReadKey();
        }
    }
}
```

### **6. Hàm xây dựng và hàm hủy trong c#**

#### **6.1 Hàm xây dựng**

Trong `C#` constructor là một phương thức đặc biệt được gọi tự động tại thời điểm đối tượng được tạo ra.
Mục đích của constructor dùng để khởi tạo dưc liệu cho dữ liệu thành viên
Constructor phải trùng tên với lớp và khồng có kiểu dữ liệu trả về
Trong `C#` có 2 loại constructor đó là: - Constructor mặc định - Constructor có đối số

**Constructor mặc định**
Một constructor không có đối số hay còn gọi là constructor mặc định. Nó được gọi tại thời điểm tạo đối tượng.
Nếu kkhoong cung cấp hàm tạo cho lớp cha của mình, C# sẽ tạo một hàm theo mặc định để khởi tạo đối tượng và đặt các biến thành viên thành các giá trị mặc định tùy thuộc vào kiểu dữ liệu của nó.
Mình sẽ liệt kê giá trị mặc định của môt số kiểu dữ liệu mặc định hay sử dụng sau:
| Kiểu dữ liệu | Giá trị mặc định |
|:-------------|:-----------------|
| bool | false |
| float | 0.0F |
| int | 0 |
| byte | 0 |
| decimal | 0M |
| long | 0L |
| char | '\0' |

```
using System;
namespace ConsoleApp1
{
    class People
    {
        int old;
        string name;
        double height;
        public People()
        {
            Console.WriteLine("Goi ham xay dung mac nhien");
            Console.WriteLine("Name" + name);
            Console.WriteLine("Old: " + old);
            Console.WriteLine("height: " + height);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            People p = new People();
            Console.ReadKey();
        }
    }
}
```

![](https://freetuts.net/upload/tut_post/images/2019/03/10/1668/cshaprp_cons1.PNG)

#### **6.2 Hàm xây dựng có tham số**

Một constructor có tham số được gọi là constructor có tham số
Nó được sử dụng để cung cấp các giá trị khác nhau cho các đối tượng riêng biệt

```
using System;
namespace ConsoleApp1
{
    class People
    {
        int old;
        string name;
        double height;
        public People()
        {
            Console.WriteLine("\n---Goi ham xay dung mac nhien---");
        }
        public People(int old, string name, double height)
        {
            Console.WriteLine("\n---Goi ham xay dung co 3 tham so---");
            this.old = old;
            this.name = name;
            this.height = height;
        }
        public People(int old, string name)
        {
            Console.WriteLine("\n---Goi ham xay dung co 2 tham so---");
            this.old = old;
            this.name = name;
        }
        public void Show()
        {
            Console.WriteLine("Old: " + old + ",\nName: " + name + ",\nHeight: " + height);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            People p = new People();
            p.Show();
            People p1 = new People(20, "Nguyen Van A", 180);
            p1.Show();
            People p2 = new People(18, "Nguyen Van A");
            p2.Show();
            Console.ReadKey();
        }
    }
}
```

![](https://freetuts.net/upload/tut_post/images/2019/03/10/1668/a.PNG)

#### **6.3 Hàm xây dựng có tham số**

Một hàm hủy hoạt động ngược lại với hàm tạo. Nó phá hủy các đối tượng của các lớp. Nó chỉ có thể được định nghĩa một lần trong một lớp. Giống như các hàm xây dựng, hàm hủy được gọi tự động.

```
using System;
namespace ConsoleApp1
{
    class People
    {
        public People()
        {
            Console.WriteLine("\n---Goi ham xay dung mac nhien---");
        }
        ~People()
        {
            Console.WriteLine("\n---Goi ham huy---");
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            People p = new People();
            Console.ReadKey();
        }
    }
}
```

Điểm lưu ý:

- Hàm hủy là duy nhát cho lớp của nó, tức là không thể có nhiều hơn một hàm hủy trong một lớp.
- Hàm hủy không có kiểu giá trị trả về và có cùng tên với tên lớp
- Hàm hủy được phân biệt với một hàm xây dựng vì ký hiệu `~` trước tên của nó
- Hàm hủy không chấp nhận bất kỳ tham số nào và không được sửa đổi hàm hủy
- Hàm hủy không thể được định nghĩa trong cấu trúc. Hàm hủy chỉ được sử dụng với các lớp.
- Hàm hủy không thể bị overloaded hoặc kế thừa - Hàm hủy được gọi khi chương trình thoát
  Destructor được gọi là ngầm định bởi trình thu thập Rác .NET framework và do đó, chúng ta không cần quan tâm đến hàm hủy này làm gì..

### **7. Tìm hiểu từ khóa this và static trong c#**

#### **7.1 Từ khóa this trong c#**

Trước khi tìm hiểu về từ khóa this là gì, chúng ta xem ví dụ sau đây

```
using System;
namespace ConsoleApp1
{
    class People
    {
        int old;
        string name;
        double height;
        public People(int old, string name, double height)
        {
            Console.WriteLine("\n---Goi ham xay dung co 3 tham so---");
            old = old;
            name = name;
            height = height;
        }
        public void Show()
        {
            Console.WriteLine("Old: " + old + ",\nName: " + name + ",\nHeight: " + height);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            People p1 = new People(20, "Nguyen Van A", 180);
            p1.Show();
            Console.ReadKey();
        }
    }
}
```

![](https://freetuts.net/upload/tut_post/images/2019/03/18/1688/a.PNG)

Từ kết quả trên chúng ta thấy kết quả không như chúng ta mong đợi (đáng lẻ kết quả phải là old = 20, name = Nguyen Van A, height = 180).

Như vậy khi tên tham số trùng với tên của dữ liệu thành viên của lớp, thì chương trình không hiểu nó là dữ liệu thành viên mà nó hiểu đây là tham số truyền vào.

Trong c# có từ khóa this giúp chúng ta giải quyết khó khăn trên

Chúng ta sẽ thay đổi đoạn code trên như sau:

```
using System;
namespace ConsoleApp1
{
    class People
    {
        int old;
        string name;
        double height;
        public People(int old, string name, double height)
        {
            Console.WriteLine("\n---Goi ham xay dung co 3 tham so---");
            this.old = old;
            this.name = name;
            this.height = height;
        }
        public void Show()
        {
            Console.WriteLine("Old: " + old + ",\nName: " + name + ",\nHeight: " + height);
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            People p1 = new People(20, "Nguyen Van A", 180);
            p1.Show();
            Console.ReadKey();
        }
    }
}
```

![](<https://freetuts.net/upload/tut_post/images/2019/03/18/1688/a(1).PNG>)
Như vậy chúng ta hiểu từ khóa this trong c# một cách đơn giản như sạu:
Từ khóa `this` trong `c#` được sử dụng để tham chiếu đến thể hiện (instance) hiện tại của lớp. Nó cũng được sử dụng để phân biệt giữa các tham số phương thức và các dữ liệu thành viên của lớp nếu cả hai đều có cùng tên.

#### **7.1 Từ khóa static trong c#**

Static ở đây là thuộc về lớp, không thuộc về thể hiện của lớp nữa. Vì vậy khi khởi tạo đối tượng thì biến static không được khởi tạo theo đối tượng.
Trong C#, static có thể là field, method, constructor, class, properties, operator và event. Trong nội dung bài này chúng ta chỉ cùng tìm hiểu về 2 loại static đó là static field và static class.
**Static Field**
Một trường được khai báo có từ khóa static trước tên trường, được gọi là trường tĩnh (static field). Không giống như trường bình thường của đối tượng là nhận bộ nhớ mỗi lần bạn tạo đối tượng, chỉ có một bản sao của trường tĩnh được tạo trong bộ nhớ. Nó được chia sẻ cho tất cả các đối tượng.

```
using System;
namespace ConsoleApp1
{
    class People
    {
        int id;
        string name;
        static string nationality = "Viet Nam";
        public People(int id, string name)
        {
            this.id = id;
            this.name = name;

        }
        public void Show()
        {
            Console.WriteLine("Id: " + id + ",\nName: " + name + ",\nationality: " + nationality + "\n\n");
        }
    }
    class Program
    {
        static void Main(string[] args)
        {
            People p1 = new People(1, "Nguyen Van A");
            p1.Show();
            People p2 = new People(2, "Nguyen Van B");
            p2.Show();
            People p3 = new People(3, "Nguyen Van C");
            p3.Show();
            Console.ReadKey();
        }
    }
}
```

Do trường tĩnh là thuộc về lớp, nên muốn truy xuất hay thay đổi giá trị của trường tĩnh chúng ta không cần phải khởi tạo đối tượng. Chỉ cần lấy tên lớp chấm tên trường static.

```
using System;
namespace ConsoleApp1
{
    class People
    {
        int id;
        string name;
        public static string nationality = "Viet Nam";
        public People(int id, string name)
        {
            this.id = id;
            this.name = name;

        }
        public void Show()
        {
            Console.WriteLine("Id: " + id + ",\nName: " + name + ",\nationality: " + nationality + "\n");
        }

    }
    class Program
    {
        static void Main(string[] args)
        {
            People p1 = new People(1, "Nguyen Van A");
            p1.Show();
            People p2 = new People(2, "Nguyen Van B");
            p2.Show();
            People p3 = new People(3, "Nguyen Van C");

            Console.WriteLine("\n-------------Thay doi quoc tich----------------------\n");

            People.nationality = "thay doi quoc tich";
            p3.Show();
            People p4 = new People(4, "Nguyen Van D");
            p4.Show();
            People p5 = new People(5, "Nguyen Van E");
            p5.Show();
            Console.WriteLine("\n-------------hien thi gia tri cua 2 doi tuong p1 va p2----------------------\n");
            p1.Show();
            p2.Show();
            Console.ReadKey();
        }
    }
}
```

**Static class**
`static class` cũng giống như lớp khác, tuy nhiên nó không có thể hiện. Nghĩa là chúng ta không tạo được đối tượng từ static class.

Một số điểm cần lưu ý:

- static class chỉ chứa thành viên là static
- static class không có thể hiện
- static class không chứa hàm xây dựng
- chúng ta vẫn có thể gọi và sử dụng thành viên của static class

```
using System;
namespace ConsoleApp1
{
    public static class MyMath
    {
        public static float PI = 3.14f;
        public static int squared(int n) { return n * n; }
    }
    class Program
    {
        static void Main(string[] args)
        {
            int squared;
            float pi = MyMath.PI;
            squared = MyMath.squared(10);
            Console.WriteLine("squared: " + squared);
            Console.WriteLine("\nPI: " + pi);
            Console.ReadKey();
        }
    }
}
```

### **8. Tính Đóng Gói (Encapsulation)**

- Định nghĩa: Tính đóng gói là khả năng che giấu thông tin chi tiết của một đối tượng và chỉ cung cấp những gì cần thiết cho người dùng. Nó giúp bảo vệ dữ liệu khỏi bị truy cập hoặc thay đổi trực tiếp từ bên ngoài.
- Cách thực hiện:
- Sử dụng các access modifier như `private`, `protected`, `internal`, và `public`.
- Các thuộc tính (properties) thường được sử dụng để kiểm soát truy cập đến các biến thành viên (fields).

```
public class Person {
    private string name;
    public string Name {
        get { return name; }
        set { name = value; }
    }
}

```

### **9. Tính thừa kế (inheritance) trong C#**

- Trong C# thừa kế là một quá trình trong đó một đối tượng có được tất cả các thuộc thính và hành vi của đối tượng cha của nó một cách tự động. Theo cách đó, chúng ta có thể sử dụng lại, mở rộng hoặc sửa đổi các thuộc tính và hành vi đã được định nghĩa trong một lớp khác.
- Trong C#, lớp kế thừa các thành viên của lớp khác được gọi là lớp dẫn xuất(derived) và lớp có các thành viên được kế thùa được gọi là lớp cơ sở(base). Lớp dẫn xuất là lớp chuyên biệt cho lớp cơ sở.
- Cách thực hiện: Sử dụng ký hiệu dấu hai chấm `:`để chỉ ra rằng một lớp kế thừa từ một lớp khác.

```
derived_class : base_class {

}
```

Ưu điểm của thừa kế là có thể sử dụng lại các thành viên của lớp cha mà không cần phải định nghĩa lại thành viên lần nữa. Vì vậy, chương trình chúng ta sẽ ít code hơn.

### **10. Tính Đa Hình (Polymorphism)**

- Định nghĩa: Tính đa hình cho phép các đối tượng khác nhau thực thi các hành vi khác nhau thông qua cùng một giao diện. Điều này có thể đạt được thông qua phương thức ảo (virtual methods) và phương thức trừu tượng (abstract methods).
- Cách thực hiện:
- Sử dụng từ khóa `virtual` và `override` để ghi đè phương thức.
- Sử dụng từ khóa `abstract` cho các lớp và phương thức trừu tượng.

```
public class Animal {
   public virtual void MakeSound() {
       Console.WriteLine("Some generic animal sound");
   }
}

public class Dog : Animal {
   public override void MakeSound() {
       Console.WriteLine("Bark");
   }
}

public class Cat : Animal {
   public override void MakeSound() {
       Console.WriteLine("Meow");
   }
}
```

### **11. Tính Trừu Tượng (Abstraction)**

- Định nghĩa: Tính trừu tượng là khả năng ẩn giấu các chi tiết cụ thể của việc triển khai và chỉ hiển thị những phần cốt lõi của đối tượng hoặc chức năng. Nó giúp giảm độ phức tạp và tăng tính dễ hiểu cho người dùng.
- Cách thực hiện:
- Sử dụng lớp trừu tượng (abstract class) và giao diện (interface).
- Các lớp trừu tượng có thể chứa các phương thức trừu tượng và phương thức bình thường.
- Giao diện chỉ chứa các phương thức trừu tượng mà không có phần triển khai.

```
public abstract class Shape {
   public abstract void Draw();
}

public class Circle : Shape {
   public override void Draw() {
       Console.WriteLine("Drawing a circle");
   }
}

public interface IMovable {
   void Move();
}

public class Car : IMovable {
   public void Move() {
       Console.WriteLine("Car is moving");
   }
}
```

### **Design patterns**

### 12. Creational Patterns (Mẫu khởi tạo)

#### Singleton

Đảm bảo rằng một lớp chỉ có một thể hiện duy nhất và cung cấp một điểm truy cập toàn cục đến nó.

```csharp
public class Singleton {
    private static Singleton _instance;
    private static readonly object _lock = new object();

    private Singleton() {}

    public static Singleton Instance {
        get {
            if (_instance == null) {
                lock (_lock) {
                    if (_instance == null) {
                        _instance = new Singleton();
                    }
                }
            }
            return _instance;
        }
    }
}
```

#### Factory Method

Cung cấp một giao diện để tạo đối tượng, cho phép các lớp con quyết định việc tạo đối tượng nào.

```csharp
public abstract class Creator {
    public abstract IProduct FactoryMethod();

    public string SomeOperation() {
        var product = FactoryMethod();
        return "Creator: " + product.Operation();
    }
}

public class ConcreteCreatorA : Creator {
    public override IProduct FactoryMethod() {
        return new ConcreteProductA();
    }
}

public interface IProduct {
    string Operation();
}

public class ConcreteProductA : IProduct {
    public string Operation() {
        return "Result of ConcreteProductA";
    }
}
```

#### Abstract Factory

Cung cấp một giao diện để tạo ra các đối tượng thuộc các họ liên quan hoặc phụ thuộc mà không cần chỉ định lớp cụ thể của chúng.

```csharp
public interface IAbstractFactory {
    IAbstractProductA CreateProductA();
    IAbstractProductB CreateProductB();
}

public class ConcreteFactory1 : IAbstractFactory {
    public IAbstractProductA CreateProductA() {
        return new ConcreteProductA1();
    }

    public IAbstractProductB CreateProductB() {
        return new ConcreteProductB1();
    }
}

public interface IAbstractProductA {
    string UsefulFunctionA();
}

public class ConcreteProductA1 : IAbstractProductA {
    public string UsefulFunctionA() {
        return "The result of the product A1.";
    }
}

public interface IAbstractProductB {
    string UsefulFunctionB();
}

public class ConcreteProductB1 : IAbstractProductB {
    public string UsefulFunctionB() {
        return "The result of the product B1.";
    }
}
```

### 13. Structural Patterns (Mẫu cấu trúc)

#### Adapter

Cho phép các lớp có giao diện không tương thích làm việc cùng nhau bằng cách chuyển đổi giao diện của một lớp thành một giao diện khác mà một client mong đợi.

```csharp
public interface ITarget {
    string GetRequest();
}

public class Adaptee {
    public string GetSpecificRequest() {
        return "Specific request.";
    }
}

public class Adapter : ITarget {
    private readonly Adaptee _adaptee;

    public Adapter(Adaptee adaptee) {
        this._adaptee = adaptee;
    }

    public string GetRequest() {
        return $"This is '{this._adaptee.GetSpecificRequest()}'";
    }
}
```

#### Composite

Kết hợp các đối tượng thành cấu trúc cây để biểu diễn hệ thống phân cấp bộ phận-toàn thể.

```csharp
public abstract class Component {
    public abstract void Operation();
}

public class Leaf : Component {
    public override void Operation() {
        Console.WriteLine("Leaf Operation");
    }
}

public class Composite : Component {
    private List<Component> _children = new List<Component>();

    public void Add(Component component) {
        _children.Add(component);
    }

    public void Remove(Component component) {
        _children.Remove(component);
    }

    public override void Operation() {
        Console.WriteLine("Composite Operation");
        foreach (var child in _children) {
            child.Operation();
        }
    }
}
```

#### Decorator

Dynamically thêm hành vi bổ sung cho một đối tượng bằng cách bao bọc nó trong một đối tượng decorator.

```csharp
public abstract class Component {
    public abstract string Operation();
}

public class ConcreteComponent : Component {
    public override string Operation() {
        return "ConcreteComponent";
    }
}

public abstract class Decorator : Component {
    protected Component _component;

    public Decorator(Component component) {
        this._component = component;
    }

    public void SetComponent(Component component) {
        this._component = component;
    }

    public override string Operation() {
        if (this._component != null) {
            return _component.Operation();
        } else {
            return string.Empty;
        }
    }
}

public class ConcreteDecoratorA : Decorator {
    public ConcreteDecoratorA(Component comp) : base(comp) { }

    public override string Operation() {
        return $"ConcreteDecoratorA({base.Operation()})";
    }
}
```

### 14. Behavioral Patterns (Mẫu hành vi)

#### Observer

Định nghĩa một sự phụ thuộc một-nhiều giữa các đối tượng, sao cho khi một đối tượng thay đổi trạng thái, tất cả các phụ thuộc của nó đều được thông báo và cập nhật tự động.

```csharp
public interface IObserver {
    void Update(ISubject subject);
}

public interface ISubject {
    void Attach(IObserver observer);
    void Detach(IObserver observer);
    void Notify();
}

public class ConcreteSubject : ISubject {
    public int State { get; set; } = -0;

    private List<IObserver> _observers = new List<IObserver>();

    public void Attach(IObserver observer) {
        Console.WriteLine("Subject: Attached an observer.");
        this._observers.Add(observer);
    }

    public void Detach(IObserver observer) {
        this._observers.Remove(observer);
        Console.WriteLine("Subject: Detached an observer.");
    }

    public void Notify() {
        Console.WriteLine("Subject: Notifying observers...");
        foreach (var observer in _observers) {
            observer.Update(this);
        }
    }

    public void SomeBusinessLogic() {
        Console.WriteLine("\nSubject: I'm doing something important.");
        this.State = new Random().Next(0, 10);
        Console.WriteLine("Subject: My state has just changed to: " + this.State);
        this.Notify();
    }
}

public class ConcreteObserverA : IObserver {
    public void Update(ISubject subject) {
        if ((subject as ConcreteSubject).State < 3) {
            Console.WriteLine("ConcreteObserverA: Reacted to the event.");
        }
    }
}
```

#### Command

Đóng gói một yêu cầu dưới dạng một đối tượng, cho phép bạn tham số hóa khách hàng với các yêu cầu khác nhau, hàng đợi hoặc ghi nhật ký các yêu cầu, và hỗ trợ các thao tác có thể hoàn tác.

```csharp
public interface ICommand {
    void Execute();
}

public class SimpleCommand : ICommand {
    private string _payload;

    public SimpleCommand(string payload) {
        this._payload = payload;
    }

    public void Execute() {
        Console.WriteLine($"SimpleCommand: See, I can do simple things like printing ({this._payload})");
    }
}

public class ComplexCommand : ICommand {
    private Receiver _receiver;

    private string _a;

    private string _b;

    public ComplexCommand(Receiver receiver, string a, string b) {
        this._receiver = receiver;
        this._a = a;
        this._b = b;
    }

    public void Execute() {
        Console.WriteLine("ComplexCommand: Complex stuff should be done by a receiver object.");
        this._receiver.DoSomething(this._a);
        this._receiver.DoSomethingElse(this._b);
    }
}

public class Receiver {
    public void DoSomething(string a) {
        Console.WriteLine($"Receiver: Working on ({a}.)");
    }

    public void DoSomethingElse(string b) {
        Console.WriteLine($"Receiver: Also working on ({b}.)");
    }
}

public class Invoker {
    private ICommand _onStart;
    private ICommand _onFinish;

    public void SetOnStart(ICommand command) {
        this._onStart = command;
    }

    public void SetOnFinish(ICommand command) {
        this._onFinish = command;
    }

    public void DoSomethingImportant() {
        Console.WriteLine("Invoker: Does anybody want something done before I begin?");
        if (this._onStart is ICommand) {
            this._onStart.Execute();
        }

        Console.WriteLine("Invoker: ...doing something really important...");

        Console.WriteLine("Invoker: Does anybody want something done after I finish?");
        if (this._onFinish is ICommand) {
            this._onFinish.Execute();
        }
    }
}
```

#### Tổng Kết

Các design patterns trên chỉ là một phần nhỏ trong số rất nhiều mẫu thiết kế có sẵn. Chúng được thiết kế để giải quyết các vấn đề phổ biến và mang lại các giải pháp tái sử dụng, linh hoạt, và dễ bảo trì. Hiểu và áp dụng các mẫu thiết kế này trong C# sẽ giúp bạn trở thành một lập trình viên hiệu quả hơn và xây dựng các ứng dụng chất lượng cao.
