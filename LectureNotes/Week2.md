### **1. Variables (Biến)**

- **Định nghĩa:** Biến là tên đại diện cho dữ liệu lưu trữ trong bộ nhớ máy tính.
- **Cách khai báo:**

  ```java
  datatype variableName;
  ```

  - **Ví dụ:**
    ```java
    int age;         // Khai báo biến kiểu số nguyên
    double radius;   // Khai báo biến kiểu số thực
    ```

- **Gán giá trị:**

  ```java
  variableName = value;
  ```

  - **Ví dụ:**
    ```java
    age = 25;
    radius = 5.5;
    ```

- **Ý nghĩa:** Các biến giúp chương trình linh hoạt, có thể thay đổi giá trị mà không cần sửa mã nguồn.

**Ví dụ thực tế:** Tính diện tích hình tròn:

```java
double radius = 7.0; // Bán kính hình tròn
double area = radius * radius * 3.14159;
System.out.println("Area: " + area);
```

---

### **2. Numeric Data Types (Kiểu dữ liệu số)**

- **Phân loại:**

  - **Số nguyên:** `byte`, `short`, `int`, `long`.
  - **Số thực:** `float`, `double`.

- **Phạm vi giá trị:**
  - `byte`: -128 đến 127.
  - `int`: -2,147,483,648 đến 2,147,483,647.
  - `double`: Có độ chính xác cao hơn `float`.

**Ví dụ thực tế:**

```java
int population = 1000000; // Số dân
double interestRate = 4.5; // Lãi suất
```

---

### **3. Constants (Hằng số)**

- **Định nghĩa:** Giá trị không thay đổi trong suốt chương trình.
- **Cách khai báo:**
  ```java
  final datatype CONSTANTNAME = value;
  ```
  - **Ví dụ:**
    ```java
    final double PI = 3.14159; // Hằng số PI
    ```

**Ví dụ thực tế:**

```java
final double TAX_RATE = 0.1;
double price = 100.0;
double tax = price * TAX_RATE;
System.out.println("Tax: " + tax);
```

---

### **4. Operators (Toán tử)**

- **Loại toán tử:**
  - Số học: `+`, `-`, `*`, `/`, `%`.
  - Gán: `=`, `+=`, `-=`, ...
  - Tăng/giảm: `++`, `--`.

**Ví dụ thực tế:**

```java
int x = 5, y = 3;
x += y; // x = x + y => x = 8
System.out.println("x: " + x);
```

---

### **5. Numeric Type Conversions (Ép kiểu số học)**

- **Ép kiểu ngầm định (Widening):** Tự động chuyển từ kiểu nhỏ sang kiểu lớn hơn.

  - **Ví dụ:**
    ```java
    int a = 10;
    double b = a; // Ép kiểu int sang double
    ```

- **Ép kiểu tường minh (Narrowing):** Chuyển kiểu lớn sang nhỏ, cần khai báo rõ ràng.
  - **Ví dụ:**
    ```java
    double c = 9.8;
    int d = (int) c; // Ép kiểu double sang int
    ```

---

### **6. Coding Conventions (Quy tắc đặt tên)**

- **Biến:** camelCase (chữ cái đầu tiên viết thường, từ tiếp theo viết hoa).
  - **Ví dụ:** `studentAge`, `totalAmount`.
- **Hằng số:** SCREAMING_SNAKE_CASE (viết hoa toàn bộ, phân cách bằng dấu gạch dưới).
  - **Ví dụ:** `PI`, `MAX_VALUE`.
