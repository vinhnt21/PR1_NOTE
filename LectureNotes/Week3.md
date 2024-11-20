### **1. Mathematical Functions (Hàm toán học)**

- **Hàm thường dùng:**

  - `Math.pow(a, b)`: Lũy thừa \( a^b \).
  - `Math.sqrt(a)`: Căn bậc hai.
  - `Math.abs(a)`: Giá trị tuyệt đối.
  - `Math.min(a, b) / Math.max(a, b)`: Tìm giá trị nhỏ nhất/lớn nhất.

- **Ví dụ:**

  ```java
  System.out.println(Math.pow(2, 3)); // 8.0
  System.out.println(Math.abs(-5));  // 5
  ```

- **Sinh số ngẫu nhiên:**
  ```java
  int randomNum = 1 + (int)(Math.random() * 10); // Từ 1 đến 10
  ```

---

### **2. Character Datatype & Operations (Kiểu dữ liệu ký tự)**

- **Đặc điểm:**

  - Sử dụng kiểu `char` để biểu diễn ký tự.
  - Ký tự Unicode giúp hỗ trợ nhiều ngôn ngữ.

- **Ví dụ:**

  ```java
  char letter = 'A';
  char unicodeLetter = '\u0041'; // Ký tự 'A'
  System.out.println(letter == unicodeLetter); // true
  ```

- **Phép toán trên ký tự:**
  ```java
  char ch = 'a';
  System.out.println(++ch); // 'b'
  System.out.println('a' < 'b'); // true
  ```

---

### **3. The String Type (Chuỗi ký tự)**

- **Đặc điểm:**

  - Kiểu dữ liệu `String` dùng để biểu diễn chuỗi ký tự.
  - Không phải kiểu nguyên thủy mà là lớp.

- **Các thao tác cơ bản:**
  - Lấy độ dài chuỗi:
    ```java
    String s = "Java";
    System.out.println(s.length()); // 4
    ```
  - Nối chuỗi:
    ```java
    String s1 = "Hello";
    String s2 = "World";
    System.out.println(s1 + " " + s2); // Hello World
    ```
  - Chuyển đổi chữ hoa/thường:
    ```java
    System.out.println("Java".toUpperCase()); // JAVA
    ```

---

### **4. Selections (Câu lệnh điều kiện)**

- **Kiểu điều kiện:**
  - **One-way if:** Thực hiện nếu điều kiện đúng.
    ```java
    if (x > 0) {
        System.out.println("Positive number");
    }
    ```
  - **Two-way if-else:** Chọn giữa hai luồng.
    ```java
    if (x > 0) {
        System.out.println("Positive");
    } else {
        System.out.println("Negative");
    }
    ```
  - **Nested if:** Lồng nhiều điều kiện.
    ```java
    if (x > 0) {
        if (y > 0) System.out.println("Both positive");
    }
    ```

---

### **5. Switch Statement (Câu lệnh switch)**

- **Cách sử dụng:**

  ```java
  switch (day) {
      case 1: System.out.println("Monday"); break;
      case 2: System.out.println("Tuesday"); break;
      default: System.out.println("Invalid day");
  }
  ```

- **Lưu ý:**
  - Dùng `break` để tránh "fall-through".
  - Hỗ trợ `int`, `char`, `String`.

---

### **6. Ternary Operator (Toán tử ba ngôi)**

- **Cách sử dụng:**

  ```java
  int max = (a > b) ? a : b;
  System.out.println(max);
  ```

- **Ví dụ thực tế:**
  ```java
  System.out.println((x % 2 == 0) ? "Even" : "Odd");
  ```

---

### **7. Common Errors and Pitfalls (Lỗi thường gặp)**

1. **Quên dấu ngoặc nhọn:**
   ```java
   if (x > 0)
       System.out.println("Positive");
       System.out.println("Always executed"); // Sai logic
   ```
2. **Dùng sai dấu `=` thay vì `==`:**

   ```java
   if (x = 1) // Sai cú pháp
   ```

3. **Kiểm tra sai giá trị số thực:**
   ```java
   double x = 0.1 + 0.2;
   if (x == 0.3) // Sai do lỗi làm tròn
   ```

---

### **8. Final Touches**

- **Tối ưu code:**
  - **Tránh lặp mã:**
    ```java
    int tuition = (inState) ? 5000 : 15000;
    System.out.println("The tuition is " + tuition);
    ```
