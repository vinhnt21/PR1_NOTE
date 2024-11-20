### **1. Recursion (Đệ quy)**

#### **1.1. Khái niệm**

- **Định nghĩa:** Phương thức tự gọi chính nó để giải quyết bài toán nhỏ hơn của cùng một vấn đề.
- **Hai phần chính:**
  - **Base Case:** Điều kiện dừng để tránh vòng lặp vô hạn.
  - **Recursive Case:** Chia bài toán lớn thành các bài toán nhỏ hơn và giải quyết chúng đệ quy.

#### **1.2. Ví dụ**

- **Tính giai thừa:**
  ```java
  public static int factorial(int n) {
      if (n == 1) return 1; // Base Case
      return n * factorial(n - 1); // Recursive Case
  }
  ```
- **Kiểm tra chuỗi palindrome:**
  ```java
  public static boolean isPalindrome(String s) {
      if (s.length() <= 1) return true; // Base Case
      return s.charAt(0) == s.charAt(s.length() - 1) &&
             isPalindrome(s.substring(1, s.length() - 1)); // Recursive Case
  }
  ```

#### **1.3. Các loại đệ quy**

- **Direct Recursion:** Phương thức tự gọi chính nó.
- **Indirect Recursion:** Một phương thức gọi phương thức khác và cuối cùng quay lại phương thức ban đầu.

---

### **2. Exception Handling (Xử lý ngoại lệ)**

#### **2.1. Khái niệm**

- **Exception:** Sự kiện bất ngờ làm gián đoạn chương trình.
- **Hai loại:**
  - **Checked Exceptions:** Kiểm tra tại thời điểm biên dịch.
  - **Unchecked Exceptions:** Xảy ra khi chạy, không cần kiểm tra khi biên dịch.

#### **2.2. Cách xử lý ngoại lệ**

- **Dùng try-catch:**

  ```java
  try {
      int result = 10 / 0;
  } catch (ArithmeticException e) {
      System.out.println("Cannot divide by zero!");
  }
  ```

- **Finally block:** Đảm bảo mã được thực thi dù có ngoại lệ hay không.
  ```java
  try {
      // Code
  } catch (Exception e) {
      // Handle exception
  } finally {
      System.out.println("Always executed");
  }
  ```

#### **2.3. Các ngoại lệ phổ biến**

- **ArithmeticException:** Chia cho 0.
- **ArrayIndexOutOfBoundsException:** Truy cập ngoài phạm vi mảng.
- **NullPointerException:** Thao tác trên đối tượng `null`.
- **InputMismatchException:** Kiểu nhập không khớp.

---

### **3. Text I/O (Đọc/ghi tệp văn bản)**

#### **3.1. Ghi dữ liệu vào tệp**

- **Sử dụng PrintWriter:**

  ```java
  import java.io.PrintWriter;

  public class WriteToFile {
      public static void main(String[] args) throws Exception {
          PrintWriter output = new PrintWriter("output.txt");
          output.println("Hello, World!");
          output.close();
      }
  }
  ```

#### **3.2. Đọc dữ liệu từ tệp**

- **Sử dụng Scanner:**

  ```java
  import java.io.File;
  import java.util.Scanner;

  public class ReadFromFile {
      public static void main(String[] args) throws Exception {
          File file = new File("output.txt");
          Scanner input = new Scanner(file);
          while (input.hasNext()) {
              System.out.println(input.nextLine());
          }
          input.close();
      }
  }
  ```

---

### **4. Enums (Kiểu liệt kê)**

#### **4.1. Định nghĩa**

- **Enum:** Tập hợp các hằng số được định nghĩa trước.
- **Cách khai báo:**
  ```java
  enum Day { MONDAY, TUESDAY, WEDNESDAY, THURSDAY, FRIDAY, SATURDAY, SUNDAY }
  ```

#### **4.2. Sử dụng với switch-case**

- **Ví dụ:**
  ```java
  Day today = Day.MONDAY;
  switch (today) {
      case MONDAY:
          System.out.println("Start of the week!");
          break;
      case FRIDAY:
          System.out.println("Almost weekend!");
          break;
      default:
          System.out.println("Midweek");
  }
  ```
