#### **1. Two Sum**

- **Mô tả:** Tìm hai số trong mảng có tổng bằng giá trị mục tiêu.
- **Code:**

```java
public static int[] twoSum(int[] nums, int target) {
    for (int i = 0; i < nums.length; i++) {
        for (int j = i + 1; j < nums.length; j++) {
            if (nums[i] + nums[j] == target) {
                return new int[] {i, j};
            }
        }
    }
    return new int[] {};
}
```

---

#### **2. Reverse String**

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

---

#### **3. Merge Two Sorted Arrays**

- **Mô tả:** Hợp nhất hai mảng đã được sắp xếp thành một mảng sắp xếp.
- **Code:**

```java
public static int[] mergeSortedArrays(int[] nums1, int[] nums2) {
    int[] merged = new int[nums1.length + nums2.length];
    int i = 0, j = 0, k = 0;
    while (i < nums1.length && j < nums2.length) {
        if (nums1[i] < nums2[j]) {
            merged[k++] = nums1[i++];
        } else {
            merged[k++] = nums2[j++];
        }
    }
    while (i < nums1.length) merged[k++] = nums1[i++];
    while (j < nums2.length) merged[k++] = nums2[j++];
    return merged;
}
```

---

#### **4. Valid Parentheses**

- **Mô tả:** Kiểm tra chuỗi ký tự ngoặc có hợp lệ không.
- **Code:**

```java
public static boolean isValid(String s) {
    Stack<Character> stack = new Stack<>();
    for (char c : s.toCharArray()) {
        if (c == '(' || c == '{' || c == '[') {
            stack.push(c);
        } else {
            if (stack.isEmpty()) return false;
            char top = stack.pop();
            if ((c == ')' && top != '(') || (c == '}' && top != '{') || (c == ']' && top != '[')) {
                return false;
            }
        }
    }
    return stack.isEmpty();
}
```

---

#### **5. Remove Duplicates from Sorted Array**

- **Mô tả:** Loại bỏ các phần tử trùng lặp trong mảng đã sắp xếp.
- **Code:**

```java
public static int removeDuplicates(int[] nums) {
    if (nums.length == 0) return 0;
    int uniqueIndex = 0;
    for (int i = 1; i < nums.length; i++) {
        if (nums[i] != nums[uniqueIndex]) {
            uniqueIndex++;
            nums[uniqueIndex] = nums[i];
        }
    }
    return uniqueIndex + 1;
}
```

---

#### **6. Best Time to Buy and Sell Stock**

- **Mô tả:** Tìm lợi nhuận tối đa có thể từ việc mua và bán cổ phiếu.
- **Code:**

```java
public static int maxProfit(int[] prices) {
    int minPrice = Integer.MAX_VALUE;
    int maxProfit = 0;
    for (int price : prices) {
        if (price < minPrice) {
            minPrice = price;
        } else if (price - minPrice > maxProfit) {
            maxProfit = price - minPrice;
        }
    }
    return maxProfit;
}
```

---

#### **7. Find Intersection of Two Arrays**

- **Mô tả:** Tìm các phần tử chung giữa hai mảng.
- **Code:**

```java
public static int[] intersection(int[] nums1, int[] nums2) {
    Set<Integer> set1 = new HashSet<>();
    Set<Integer> result = new HashSet<>();
    for (int num : nums1) set1.add(num);
    for (int num : nums2) {
        if (set1.contains(num)) result.add(num);
    }
    int[] intersection = new int[result.size()];
    int i = 0;
    for (int num : result) intersection[i++] = num;
    return intersection;
}
```

---

#### **8. Palindrome Number**

- **Mô tả:** Kiểm tra xem số nguyên có phải là palindrome.
- **Code:**

```java
public static boolean isPalindrome(int x) {
    if (x < 0) return false;
    int reversed = 0, original = x;
    while (x != 0) {
        int digit = x % 10;
        reversed = reversed * 10 + digit;
        x /= 10;
    }
    return original == reversed;
}
```

---

#### **9. FizzBuzz**

- **Mô tả:** In các số từ 1 đến n, thay "Fizz" nếu chia hết cho 3, "Buzz" nếu chia hết cho 5.
- **Code:**

```java
public static List<String> fizzBuzz(int n) {
    List<String> result = new ArrayList<>();
    for (int i = 1; i <= n; i++) {
        if (i % 3 == 0 && i % 5 == 0) {
            result.add("FizzBuzz");
        } else if (i % 3 == 0) {
            result.add("Fizz");
        } else if (i % 5 == 0) {
            result.add("Buzz");
        } else {
            result.add(String.valueOf(i));
        }
    }
    return result;
}
```

---

#### **10. Binary Search**

- **Mô tả:** Tìm một phần tử trong mảng đã sắp xếp bằng tìm kiếm nhị phân.
- **Code:**

```java
public static int binarySearch(int[] nums, int target) {
    int left = 0, right = nums.length - 1;
    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (nums[mid] == target) return mid;
        if (nums[mid] < target) left = mid + 1;
        else right = mid - 1;
    }
    return -1;
}
```
