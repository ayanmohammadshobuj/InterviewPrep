### Title: Array Example

```java
package com.fooddelivery;

public class Array {
    public static void main(String[] args) {
        // sorting an array
        int[] arr = { 13, 7, 6, 45, 21, 9, 101, 102 };
        int temp = 0;
        System.out.println("Elements of original array: ");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
        for (int i = 0; i < arr.length; i++) {
            for (int j = i + 1; j < arr.length; j++) {
                if (arr[i] > arr[j]) {
                    temp = arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
        System.out.println("\nElements of array sorted in ascending order: ");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }

        // finding the largest element
        int max = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > max) {
                max = arr[i];
            }
        }

        System.out.println("\nLargest element: " + max);

        // finding the smallest element
        int min = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] < min) {
                min = arr[i];
            }
        }

        System.out.println("Smallest element: " + min);

        // finding the sum of elements
        int sum = 0;
        for (int i = 0; i < arr.length; i++) {
            sum += arr[i];
        }

        System.out.println("Sum of elements: " + sum);

        // finding the average of elements

        System.out.println("Average of elements: " + (double) sum / arr.length);

        // finding the second largest element
        int secondMax = arr[0];
        for (int i = 1; i < arr.length; i++) {
            if (arr[i] > secondMax && arr[i] < max) {
                secondMax = arr[i];
            }
        }

        System.out.println("Second largest element: " + secondMax);

    }
}
```

### Title: Binary Search Example

```java
package com.fooddelivery;

public class BinarySearchExample {
    public static void main(String[] args) {
        int[] arr = {2, 3, 4, 10, 40};
        int target = 10;
        int result = binarySearch(arr, target);

        if (result == -1) {
            System.out.println("Element not present in array");
        } else {
            System.out.println("Element found at index: " + result);
        }
    }

    static int binarySearch(int[] arr, int target) {
        int left = 0, right = arr.length - 1;
        while (left <= right) {
            int mid = left + (right - left) / 2;

            // Check if target is present at mid
            if (arr[mid] == target) {
                return mid;
            }

            // If target greater, ignore left half
            if (arr[mid] < target) {
                left = mid + 1;
            } else {
                // If target is smaller, ignore right half
                right = mid - 1;
            }
        }

        // Target not present in array
        return -1;
    }
}
```

### Title: Exceptions Handling Example

```java
package com.fooddelivery;

public class ExceptionsHandlingExample {
    public static void main(String[] args) {
        try {
            int[] arr = new int[5];
            System.out.println(arr[6]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index is out of bounds");
        }

        System.out.println("Rest of the code");


        try {
            int a = 30, b = 0;
            int c = a / b;
            System.out.println("Result: " + c);
        } catch (ArithmeticException e) {
            System.out.println("Can't divide a number by 0");
        }

        System.out.println("Rest of the code");

        try {
            String str = null;
            System.out.println(str.length());
        } catch (NullPointerException e) {
            System.out.println("NullPointerException..");
        }

        System.out.println("Rest of the code");

        try {
            String str = "abc";
            int num = Integer.parseInt(str);
            System.out.println(num);
        } catch (NumberFormatException e) {
            System.out.println("Number format exception");
        }

        System.out.println("Rest of the code");

        try {
            int[] arr = new int[5];
            System.out.println(arr[6]);
        } catch (Exception e) {
            System.out.println("Parent exception");
        }

        System.out.println("Rest of the code");

        try {
            int[] arr = new int[5];
            System.out.println(arr[6]);
        } catch (ArrayIndexOutOfBoundsException e) {
            System.out.println("Array index is out of bounds");
        } catch (Exception e) {
            System.out.println("Parent exception");
        }
    }
}
```

### Title: Fibonacci Example

```java
package com.fooddelivery;

import java.util.Scanner;

public class Fabonacci {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter number of terms: ");
        int n = scanner.nextInt();
        scanner.close();
        int t1 = 0, t2 = 1;
        System.out.print("First " + n + " terms: ");
        for (int i = 1; i <= n; ++i) {
            System.out.print(t1 + ", ");
            int sum = t1 + t2;
            t1 = t2;
            t2 = sum;
        }
    }
}
```

### Title: HashMap Example

```java
package com.fooddelivery;
import java.util.HashMap;
import java.util.Map;

public class HashMapExample {
    public static void main(String[] args) {
        Map<String, Integer> map = new HashMap<>();
        map.put("Apple", 1);
        map.put("Banana", 2);
        map.put("Cherry", 3);

        // Fast lookup by key
        if (map.containsKey("Banana")) {
            System.out.println("Banana is present with value: " + map.get("Banana"));
        }

        // Iterating over the map
        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

### Title: HashSet Example

```java
package com.fooddelivery;
import java.util.HashSet;
import java.util.Set;

public class HashSetExample {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();
        set.add("Apple");
        set.add("Banana");
        set.add("Cherry");

        // Fast lookup
        if (set.contains("Banana")) {
            System.out.println("Banana is present in the set.");
        }

        // Iterating over the set
        for (String item : set) {
            System.out.println(item);
        }
    }
}
```

### Title: List Example

```java
package com.fooddelivery;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class ListExample {
    // List Example
    public static void main(String[] args) {

        // Creating a list
        List<String> list = new ArrayList<>();

        // Adding elements in the list
        list.add("Mango");
        list.add("Apple");
        list.add("Banana");
        list.add("Grapes");

        // Traversing list through Iterator
        Iterator<String> itr = list.iterator();

        while (itr.hasNext()) {
            System.out.println(itr.next());
        }
    }
}
```

### Title: Map Example

```java
package com.fooddelivery;

import java.util.HashMap;
import java.util.Map;

public class MapExample {
    public static void main(String[] args) {
         Map<String, String> map = new HashMap<String, String>();
         map.put("Apple", "Red");
         map.put("Banana", "Yellow");
         map.put("Mango", "Green");
         map.put("Orange", "Orange");
         map.put("Peach", "Pink");
         map.put("Pineapple", "Brown");
         map.put("Strawberry", "Red");
         map.put("Watermelon", "Green");
         System.out.println(map);
         map.remove("Peach");
         System.out.println(map);
         System.out.println(map.containsKey("Banana"));
         System.out.println(map.size());
         map.clear();
         System.out.println(map);
    }
}
```

### Title: Merge Sort Example

```java
package com.fooddelivery;

public class MergeSortExample {
    public static void main(String[] args) {
        int[] arr = {12, 11, 13, 5, 6, 7};
        int n = arr.length;

        mergeSort(arr, 0, n - 1);

        System.out.println("Sorted array:");
        for (int num : arr) {
            System.out.print(num + " ");
        }
    }

    static void mergeSort(int[] arr, int left, int right) {
        if (left < right) {
            int mid = (left + right) / 2;

            mergeSort(arr, left, mid);
            mergeSort(arr, mid + 1, right);

            merge(arr, left, mid, right);
        }
    }

    static void merge(int[] arr, int left, int mid, int right) {
        int n1 = mid - left + 1;
        int n2 = right - mid;

        int[] L = new int[n1];
        int[] R = new int[n2];

        for (int i = 0; i < n1; ++i)
            L[i] = arr[left + i];
        for (int j = 0; j < n2; ++j)
            R[j] = arr[mid + 1 + j];

        int i = 0, j = 0;
        int k = left;
        while (i < n1 && j < n2) {
            if (L[i] <= R[j]) {
                arr[k] = L[i];
                i++;
            } else {
                arr[k] = R[j];
                j++;
            }
            k++;
        }

        while (i < n1) {
            arr[k] = L[i];
            i++;
            k++;
        }

        while (j < n2) {
            arr[k] = R[j];
            j++;
            k++;
        }
    }
}
```

### Title: Method Overloading Example

```java
package com.fooddelivery;

public class MethodOverloading {
    public static void main(String[] args) {
        int a = 11;
        int b = 6;
        double c = 7.3;
        double d = 9.4;
        int result1 = minFunction(a, b);
        double result2 = minFunction(c, d);
        System.out.println("Minimum Value = " + result1);
        System.out.println("Minimum Value = " + result2);
    }

    public static int minFunction(int n1, int n2) {
        int min;
        if (n1 > n2)
            min = n2;
        else
            min = n1;

        return min;
    }

    public static double minFunction(double n1, double n2) {
        double min;
        if (n1 > n2)
            min = n2;
        else
            min = n1;

        return min;
    }
}
```

### Title: MultiThreading Example

```java
package com.fooddelivery;

public class MultiThreading {

    public static void main(String[] args) {
        Thread thread1 = new Thread(() -> {
            for (int i = 0; i < 5; i++) {
                System.out.println("Thread 1: " + i);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });

        Thread thread2 = new Thread(() -> {
            for (int i = 0; i < 5; i++) {
                System.out.println("Thread 2: " + i);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });

        thread1.start();
        thread2.start();
    }
}
```

### Title: MultiThreading2 Example

```java
package com.fooddelivery;

public class MultiThreading2 {
    public static void main(String[] args) {
        Thread thread1 = new Thread(() -> {
            for (int i = 0; i < 5; i++) {
                System.out.println("Thread 1: " + i);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });

        Thread thread2 = new Thread(() -> {
            for (int i = 0; i < 5; i++) {
                System.out.println("Thread 2: " + i);
                try {
                    Thread.sleep(1000);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }
        });

        thread1.start();
        thread2.start();
    }
}
```

### Title: Queue Example

```java
package com.fooddelivery;

import java.util.LinkedList;
import java.util.Queue;

public class QueueExample {
    public static void main(String[] args) {
        Queue<String> queue = new LinkedList<String>();
        queue.add("Apple");
        queue.add("Banana");
        queue.add("Watermelon");
        queue.add("Mango");
        queue.add("Peach");
        queue.add("Orange");
        queue.add("Pineapple");
        queue.add("Strawberry");
        System.out.println(queue);
        queue.remove("Peach");
        System.out.println(queue);
        System.out.println(queue.contains("Banana"));
        System.out.println(queue.size());
        queue.clear();
        System.out.println(queue);
    }
}
```

### Title: Quick Sort Example

```java
package com.fooddelivery;

public class QuickSortExample {
    public static void main(String[] args) {
        int[] arr = {10, 7, 8, 9, 1, 5};
        int n = arr.length;

        quickSort(arr, 0, n - 1);

        System.out.println("Sorted array:");
        for (int num : arr) {
            System.out.print(num + " ");
        }
    }

    static void quickSort(int[] arr, int low, int high) {
        if (low < high) {
            int pi = partition(arr, low, high);

            quickSort(arr, low, pi - 1);
            quickSort(arr, pi + 1, high);
        }
    }

    static int partition(int[] arr, int low, int high) {
        int pivot = arr[high];
        int i = (low - 1);
        for (int j = low; j < high; j++) {
            if (arr[j] < pivot) {
                i++;
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }

        int temp = arr[i + 1];
        arr[i + 1] = arr[high];
        arr[high] = temp;

        return i + 1;
    }
}
```

### Title: Set Example

```java
package com.fooddelivery;

import java.util.HashSet;
import java.util.Set;

public class SetExample {
    public static void main(String[] args) {
        Set<String> set = new HashSet<String>();
        set.add("Apple");
        set.add("Banana");
        set.add("Mango");
        set.add("Orange");
        set.add("Peach");
        set.add("Pineapple");
        set.add("Strawberry");
        set.add("Watermelon");
        System.out.println(set);
        set.remove("Peach");
        System.out.println(set);
        System.out.println(set.contains("Banana"));
        System.out.println(set.size());
        set.clear();
        System.out.println(set);
    }
}
```

### Title: Stacks Example

```java
package com.fooddelivery;

import java.util.Stack;

public class StacksExample {
    public static void main(String[] args) {
        Stack<String> stack = new Stack<>();

        // Push elements onto the stack
        stack.push("Cherry");
        stack.push("Apple");
        stack.push("Banana");
        stack.push("Cherry");
        stack.push("Cherry");


        // Pop elements from the stack
        while (!stack.isEmpty()) {
            System.out.println(stack.pop());
        }
    }
}
```

### Title: Two Sum Example

```java
package com.fooddelivery;

import java.util.HashMap;
import java.util.Map;

public class TwoSum {
    // Two Sum problem solution faster than O(n^2)
    public int[] twoSum(int[] nums, int target) {
        int[] result = new int[2];
        Map<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int diff = target - nums[i];
            if (map.containsKey(diff)) {
                result[0] = map.get(diff);
                result[1] = i;
                return result;
            }
            map.put(nums[i], i);
        }
        return result;
    }

    public static void main(String[] args) {
        TwoSum twoSum = new TwoSum();
        int[] nums = { 3, 4, 4, 15 };
        int target = 8;
        int[] result = twoSum.twoSum(nums, target);
        System.out.println("Indices of the two numbers such that they add up to a specific target: ");

        for (int i = 0; i < result.length; i++) {
            System.out.print(result[i] + " ");
        }

    }
}
```

### Title: Main Example

```java
package com.fooddelivery;

public class Main {
    public static void main(String[] args) {
        System.out.println("Hello world!");
    }
}
```
