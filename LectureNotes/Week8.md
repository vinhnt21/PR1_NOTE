### **1. Collections Framework (Framework tập hợp)**

#### **1.1. Tổng quan**

- **Khái niệm:** Tập hợp các lớp và giao diện hỗ trợ thao tác với nhóm đối tượng.
- **Các loại chính:**
  - **List:** Dữ liệu có thứ tự, cho phép trùng lặp (e.g., `ArrayList`, `LinkedList`).
  - **Set:** Chỉ chứa các giá trị không trùng lặp (e.g., `HashSet`, `TreeSet`).
  - **Queue:** Cấu trúc dữ liệu FIFO (e.g., `PriorityQueue`, `LinkedList`).
  - **Map:** Lưu trữ cặp key-value (e.g., `HashMap`, `TreeMap`).

---

### **2. Lists**

#### **2.1. ArrayList**

- **Đặc điểm:** Lưu trữ dữ liệu trong mảng có thể thay đổi kích thước.
- **Ưu điểm:** Truy cập nhanh theo chỉ số.
- **Ví dụ:**
  ```java
  ArrayList<String> cities = new ArrayList<>();
  cities.add("New York");
  cities.add("Los Angeles");
  System.out.println(cities); // [New York, Los Angeles]
  ```

#### **2.2. LinkedList**

- **Đặc điểm:** Lưu trữ dữ liệu trong danh sách liên kết.
- **Ưu điểm:** Chèn/xóa nhanh hơn `ArrayList` ở đầu hoặc cuối danh sách.
- **Ví dụ:**
  ```java
  LinkedList<String> names = new LinkedList<>();
  names.add("Alice");
  names.addFirst("Bob");
  System.out.println(names); // [Bob, Alice]
  ```

---

### **3. Stacks**

#### **3.1. Đặc điểm**

- **Nguyên lý:** LIFO (Last In, First Out).
- **Phương thức chính:** `push`, `pop`, `peek`.
- **Ví dụ:**
  ```java
  Stack<Integer> stack = new Stack<>();
  stack.push(10);
  stack.push(20);
  System.out.println(stack.pop()); // 20
  System.out.println(stack.peek()); // 10
  ```

---

### **4. Queues**

#### **4.1. Đặc điểm**

- **Nguyên lý:** FIFO (First In, First Out).
- **Phương thức chính:** `offer`, `poll`, `peek`.
- **Ví dụ:**
  ```java
  Queue<String> queue = new LinkedList<>();
  queue.offer("Task1");
  queue.offer("Task2");
  System.out.println(queue.poll()); // Task1
  ```

#### **4.2. PriorityQueue**

- **Đặc điểm:** Ưu tiên phần tử dựa trên thứ tự tự nhiên hoặc so sánh tùy chỉnh.
- **Ví dụ:**
  ```java
  PriorityQueue<Integer> pq = new PriorityQueue<>();
  pq.offer(30);
  pq.offer(10);
  pq.offer(20);
  System.out.println(pq.poll()); // 10 (ưu tiên nhỏ nhất)
  ```

---

### **5. Sets**

#### **5.1. HashSet**

- **Đặc điểm:** Không trùng lặp, không đảm bảo thứ tự.
- **Ví dụ:**
  ```java
  HashSet<String> set = new HashSet<>();
  set.add("A");
  set.add("B");
  set.add("A"); // Trùng lặp, không được thêm.
  System.out.println(set); // [A, B]
  ```

#### **5.2. TreeSet**

- **Đặc điểm:** Tự động sắp xếp các phần tử.
- **Ví dụ:**
  ```java
  TreeSet<Integer> treeSet = new TreeSet<>();
  treeSet.add(30);
  treeSet.add(10);
  treeSet.add(20);
  System.out.println(treeSet); // [10, 20, 30]
  ```

---

### **6. Maps**

#### **6.1. HashMap**

- **Đặc điểm:** Lưu trữ key-value, không đảm bảo thứ tự.
- **Ví dụ:**
  ```java
  HashMap<String, Integer> map = new HashMap<>();
  map.put("Alice", 90);
  map.put("Bob", 85);
  System.out.println(map.get("Alice")); // 90
  ```

#### **6.2. TreeMap**

- **Đặc điểm:** Key được sắp xếp theo thứ tự tự nhiên hoặc so sánh tùy chỉnh.
- **Ví dụ:**
  ```java
  TreeMap<String, Integer> treeMap = new TreeMap<>();
  treeMap.put("B", 20);
  treeMap.put("A", 10);
  System.out.println(treeMap); // {A=10, B=20}
  ```

---

### **7. Các Phương Thức Hữu Ích**

- **Sort và Shuffle:**
  ```java
  Collections.sort(list);
  Collections.shuffle(list);
  ```
- **Frequency:**
  ```java
  System.out.println(Collections.frequency(list, "A")); // Đếm số lần xuất hiện của "A".
  ```
