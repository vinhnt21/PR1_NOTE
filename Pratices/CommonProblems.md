#### **Mục lục**

1. [Xử lý mảng (Array Patterns)](#xử-lý-mảng-array-patterns)
   - [Tìm kiếm Min/Max trong mảng](#tìm-kiếm-minmax-trong-mảng)
   - [Sắp xếp mảng (Bubble Sort)](#sắp-xếp-mảng-bubble-sort)
   - [Đảo ngược mảng](#đảo-ngược-mảng)
   - [Đếm số lần xuất hiện của phần tử](#đếm-số-lần-xuất-hiện-của-phần-tử)
2. [Xử lý chuỗi (String Patterns)](#xử-lý-chuỗi-string-patterns)
   - [Đảo ngược chuỗi](#đảo-ngược-chuỗi)
   - [Kiểm tra chuỗi Palindrome](#kiểm-tra-chuỗi-palindrome)
   - [Đếm từ trong chuỗi](#đếm-từ-trong-chuỗi)
3. [Xử lý số nguyên (Math Patterns)](#xử-lý-số-nguyên-math-patterns)
   - [Kiểm tra số nguyên tố](#kiểm-tra-số-nguyên-tố)
   - [Tính giai thừa](#tính-giai-thừa)
   - [Dãy Fibonacci](#dãy-fibonacci)
4. [Sử dụng Collection Framework](#sử-dụng-collection-framework)
   - [ArrayList](#arraylist)
   - [HashMap](#hashmap)
   - [Stack](#stack)
   - [Queue](#queue)
5. [Recursive Patterns (Đệ quy)](#recursive-patterns-đệ-quy)
   - [GCD (Ước số chung lớn nhất)](#gcd-ước-số-chung-lớn-nhất)
   - [Đếm số cách đi cầu thang](#đếm-số-cách-đi-cầu-thang)

#### **1. Xử lý mảng (Array Patterns)**

##### **1.1. Tìm kiếm Min/Max trong mảng**

- **Mô tả:** Tìm giá trị nhỏ nhất/lớn nhất trong mảng.
- **Code:**

```java
public static int findMin(int[] nums) {
    int min = nums[0];
    for (int num : nums) {
        if (num < min) min = num;
    }
    return min;
}

public static int findMax(int[] nums) {
    int max = nums[0];
    for (int num : nums) {
        if (num > max) max = num;
    }
    return max;
}
```

##### **1.2. Sắp xếp mảng (Bubble Sort)**

- **Mô tả:** Sắp xếp mảng theo thứ tự tăng dần.
- **Code:**

```java
public static void bubbleSort(int[] nums) {
    int n = nums.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (nums[j] > nums[j + 1]) {
                int temp = nums[j];
                nums[j] = nums[j + 1];
                nums[j + 1] = temp;
            }
        }
    }
}
```

##### **1.3. Đảo ngược mảng**

- **Mô tả:** Đảo ngược các phần tử trong mảng.
- **Code:**

```java
public static void reverseArray(int[] nums) {
    int left = 0, right = nums.length - 1;
    while (left < right) {
        int temp = nums[left];
        nums[left] = nums[right];
        nums[right] = temp;
        left++;
        right--;
    }
}
```

##### **1.4. Đếm số lần xuất hiện của phần tử**

- **Mô tả:** Đếm số lần một phần tử xuất hiện trong mảng.
- **Code:**

```java
public static Map<Integer, Integer> countFrequency(int[] nums) {
    Map<Integer, Integer> freqMap = new HashMap<>();
    for (int num : nums) {
        freqMap.put(num, freqMap.getOrDefault(num, 0) + 1);
    }
    return freqMap;
}
```

---

#### **2. Xử lý chuỗi (String Patterns)**

##### **2.1. Đảo ngược chuỗi**

- **Mô tả:** Đảo ngược các ký tự trong chuỗi.
- **Code:**

```java
public static String reverseString(String s) {
    char[] chars = s.toCharArray();
    int left = 0, right = chars.length - 1;
    while (left < right) {
        char temp = chars[left];
        chars[left] = chars[right];
        chars[right] = temp;
        left++;
        right--;
    }
    return new String(chars);
}
```

##### **2.2. Kiểm tra chuỗi Palindrome**

- **Mô tả:** Kiểm tra xem chuỗi có phải là Palindrome (đọc xuôi và ngược giống nhau).
- **Code:**

```java
public static boolean isPalindrome(String s) {
    int left = 0, right = s.length() - 1;
    while (left < right) {
        if (s.charAt(left++) != s.charAt(right--)) return false;
    }
    return true;
}
```

##### **2.3. Đếm từ trong chuỗi**

- **Mô tả:** Tách chuỗi và đếm số từ.
- **Code:**

```java
public static int countWords(String s) {
    if (s == null || s.isEmpty()) return 0;
    String[] words = s.trim().split("\\s+");
    return words.length;
}
```

---

#### **3. Xử lý số nguyên (Math Patterns)**

##### **3.1. Kiểm tra số nguyên tố**

- **Mô tả:** Kiểm tra xem số có phải là số nguyên tố.
- **Code:**

```java
public static boolean isPrime(int n) {
    if (n <= 1) return false;
    for (int i = 2; i <= Math.sqrt(n); i++) {
        if (n % i == 0) return false;
    }
    return true;
}
```

##### **3.2. Tính giai thừa**

- **Mô tả:** Tính giai thừa của một số.
- **Code:**

```java
public static int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n - 1);
}
```

##### **3.3. Dãy Fibonacci**

- **Mô tả:** Tính số Fibonacci thứ n.
- **Code:**

```java
public static int fibonacci(int n) {
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
```

---

#### **4. Sử dụng Collection Framework**

##### **4.1. ArrayList**

- **Mô tả:** Thêm và truy cập phần tử trong danh sách.
- **Code:**

```java
public static void arrayListExample() {
    ArrayList<String> list = new ArrayList<>();
    list.add("Java");
    list.add("Python");
    list.add("C++");
    System.out.println(list); // [Java, Python, C++]
}
```

##### **4.2. HashMap**

- **Mô tả:** Lưu trữ và truy cập cặp key-value.
- **Code:**

```java
public static void hashMapExample() {
    HashMap<String, Integer> map = new HashMap<>();
    map.put("Alice", 90);
    map.put("Bob", 85);
    System.out.println(map.get("Alice")); // 90
}
```

##### **4.3. Stack**

- **Mô tả:** Thao tác LIFO (Last In, First Out).
- **Code:**

```java
public static void stackExample() {
    Stack<Integer> stack = new Stack<>();
    stack.push(1);
    stack.push(2);
    stack.push(3);
    System.out.println(stack.pop()); // 3
}
```

##### **4.4. Queue**

- **Mô tả:** Thao tác FIFO (First In, First Out).
- **Code:**

```java
public static void queueExample() {
    Queue<String> queue = new LinkedList<>();
    queue.offer("Task1");
    queue.offer("Task2");
    System.out.println(queue.poll()); // Task1
}
```

---

#### **5. Recursive Patterns (Đệ quy)**

##### **5.1. GCD (Ước số chung lớn nhất)**

- **Mô tả:** Tìm GCD của hai số.
- **Code:**

```java
public static int gcd(int a, int b) {
    if (b == 0) return a;
    return gcd(b, a % b);
}
```

##### **5.2. Đếm số cách đi cầu thang**

- **Mô tả:** Một người có thể đi 1 hoặc 2 bước, tìm số cách để đi hết n bậc.
- **Code:**

```java
public static int climbStairs(int n) {
    if (n <= 1) return 1;
    return climbStairs(n - 1) + climbStairs(n - 2);
}
```









