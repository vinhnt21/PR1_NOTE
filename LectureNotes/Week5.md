### **1. Loops (Vòng lặp)**

#### **1.1. While Loop**

- **Cấu trúc:**
  ```java
  while (condition) {
      // Loop body
  }
  ```
- **Hoạt động:** Lặp lại nếu điều kiện đúng.
- **Ví dụ: Đếm ngược:**
  ```java
  int n = 5;
  while (n > 0) {
      System.out.println(n);
      n--;
  }
  System.out.println("Blastoff!");
  ```

#### **1.2. Do-While Loop**

- **Cấu trúc:**
  ```java
  do {
      // Loop body
  } while (condition);
  ```
- **Hoạt động:** Thực hiện ít nhất một lần trước khi kiểm tra điều kiện.
- **Ví dụ:**
  ```java
  int sum = 0, data;
  do {
      System.out.print("Enter a number (0 to stop): ");
      data = input.nextInt();
      sum += data;
  } while (data != 0);
  System.out.println("Sum: " + sum);
  ```

#### **1.3. For Loop**

- **Cấu trúc:**
  ```java
  for (initialization; condition; update) {
      // Loop body
  }
  ```
- **Ví dụ:** In chuỗi:
  ```java
  for (int i = 1; i <= 5; i++) {
      System.out.println("Java is fun!");
  }
  ```

#### **1.4. Nested Loops (Vòng lặp lồng nhau)**

- **Ví dụ:** Bảng cửu chương:
  ```java
  for (int i = 1; i <= 9; i++) {
      for (int j = 1; j <= 9; j++) {
          System.out.print(i * j + "\t");
      }
      System.out.println();
  }
  ```

---

### **2. Break and Continue**

- **Break:** Dừng vòng lặp ngay lập tức.
  ```java
  for (int i = 1; i <= 10; i++) {
      if (i == 5) break;
      System.out.print(i + " "); // Output: 1 2 3 4
  }
  ```
- **Continue:** Bỏ qua lần lặp hiện tại, tiếp tục vòng kế tiếp.
  ```java
  for (int i = 1; i <= 10; i++) {
      if (i == 5) continue;
      System.out.print(i + " "); // Output: 1 2 3 4 6 7 8 9 10
  }
  ```

---

### **3. Arrays (Mảng)**

#### **3.1. Khai báo và khởi tạo**

- **Cấu trúc:**
  ```java
  dataType[] arrayName = new dataType[size];
  ```
- **Ví dụ:**
  ```java
  int[] numbers = new int[5];
  numbers[0] = 10; // Gán giá trị
  ```
- **Khởi tạo rút gọn:**
  ```java
  int[] numbers = {1, 2, 3, 4, 5};
  ```

#### **3.2. Truy cập và thao tác**

- **Ví dụ: Tính tổng phần tử:**
  ```java
  int[] numbers = {1, 2, 3, 4, 5};
  int sum = 0;
  for (int num : numbers) {
      sum += num;
  }
  System.out.println("Sum: " + sum); // Output: 15
  ```

#### **3.3. Các thao tác phổ biến**

- **Tìm phần tử lớn nhất:**
  ```java
  int max = numbers[0];
  for (int num : numbers) {
      if (num > max) max = num;
  }
  ```
- **Trộn ngẫu nhiên:**
  ```java
  for (int i = numbers.length - 1; i > 0; i--) {
      int j = (int)(Math.random() * (i + 1));
      int temp = numbers[i];
      numbers[i] = numbers[j];
      numbers[j] = temp;
  }
  ```

#### **3.4. Mảng đa chiều**

- **Ví dụ: Khởi tạo ma trận:**
  ```java
  int[][] matrix = new int[2][3];
  matrix[0][0] = 1; // Gán giá trị
  ```

#### **3.5. Advanced Operations**

- **Truyền mảng vào phương thức:**
  ```java
  public static void printArray(int[] array) {
      for (int num : array) {
          System.out.print(num + " ");
      }
  }
  ```
- **Trả về mảng từ phương thức:**
  ```java
  public static int[] reverse(int[] list) {
      int[] result = new int[list.length];
      for (int i = 0; i < list.length; i++) {
          result[list.length - 1 - i] = list[i];
      }
      return result;
  }
  ```
