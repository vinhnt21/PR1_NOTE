### **1. Introduction to Methods**

- **Khái niệm:**

  - Phương thức (method) là một khối mã thực hiện một tác vụ cụ thể và có thể được gọi lại nhiều lần.
  - **Ví dụ:** Tính tổng các số từ `i1` đến `i2`:

    ```java
    public static int sum(int i1, int i2) {
        int result = 0;
        for (int i = i1; i <= i2; i++) result += i;
        return result;
    }

    public static void main(String[] args) {
        System.out.println(sum(1, 10)); // 55
    }
    ```

---

### **2. Method Structure**

- **Cấu trúc:**

  ```java
  modifier returnType methodName(parameterList) {
      // Method body
  }
  ```

  - **Modifier:** Quyền truy cập (vd: `public`, `private`).
  - **Return type:** Kiểu dữ liệu trả về (hoặc `void` nếu không trả về).
  - **Method name:** Tên phương thức.
  - **Parameter list:** Danh sách tham số (nếu có).
  - **Method body:** Nội dung thực thi.

- **Ví dụ:** Tìm số lớn hơn giữa hai số:
  ```java
  public static int max(int num1, int num2) {
      return (num1 > num2) ? num1 : num2;
  }
  ```

---

### **3. Types of Methods**

#### **Void Methods**

- **Không trả về giá trị.**
- **Ví dụ:**
  ```java
  public static void sayHello() {
      System.out.println("Hello, world!");
  }
  ```

#### **Value-Returning Methods**

- **Trả về một giá trị cụ thể.**
- **Ví dụ:**
  ```java
  public static int square(int number) {
      return number * number;
  }
  System.out.println(square(5)); // 25
  ```

---

### **4. Passing Arguments**

- **Tham số và đối số:**

  - **Tham số (parameters):** Khai báo trong phương thức.
  - **Đối số (arguments):** Giá trị thực tế truyền vào khi gọi phương thức.

- **Truyền giá trị:**
  - Java luôn sử dụng "pass-by-value".
  - **Ví dụ:**
    ```java
    public static void increment(int num) {
        num++;
    }
    int x = 5;
    increment(x);
    System.out.println(x); // 5
    ```

---

### **5. Method Features**

#### **Modularization (Tính mô-đun)**

- Giúp chia nhỏ chương trình, dễ đọc và bảo trì.
- **Ví dụ:** Kiểm tra số nguyên tố:
  ```java
  public static boolean isPrime(int num) {
      if (num <= 1) return false;
      for (int i = 2; i <= Math.sqrt(num); i++) {
          if (num % i == 0) return false;
      }
      return true;
  }
  ```

#### **Method Overloading (Nạp chồng phương thức)**

- Cùng tên nhưng khác tham số.
- **Ví dụ:**
  ```java
  public static int max(int a, int b) {
      return (a > b) ? a : b;
  }
  public static double max(double a, double b) {
      return (a > b) ? a : b;
  }
  ```

#### **Recursion (Đệ quy)**

- Phương thức tự gọi chính nó.
- **Ví dụ:** Tính giai thừa:
  ```java
  public static int factorial(int n) {
      if (n == 1) return 1;
      return n * factorial(n - 1);
  }
  System.out.println(factorial(5)); // 120
  ```

---

### **6. Summary**

- **Cách định nghĩa:**

  ```java
  public static void methodName() { ... }
  public static returnType methodName(params) { return value; }
  ```

- **Cách gọi:**
  - Với giá trị trả về:
    ```java
    int result = methodName(args);
    ```
  - Không có giá trị trả về:
    ```java
    methodName(args);
    ```
