package BZcodes;

//String -- StringBuilder demo

public class StringBuliderDemo {
        // 1. Create a StringBuilder
        public void StringBuilderClass(String args[])0 {
        StringBuilder sb = new StringBuilder("Hello");
        System.out.println("Initial StringBuilder: " + sb);
        // 2. Append - add text at the end
        sb.append(" World");
        System.out.println("After append: " + sb);
        // 3. Insert - add text at a specific index
        sb.insert(5, ",");
        System.out.println("After insert: " + sb);
        // 4. Replace - replace characters from start index to end index (exclusive)
        sb.replace(0, 5, "Hi");
        System.out.println("After replace: " + sb);
        // 5. Delete - remove characters from start index to end index (exclusive)
        sb.delete(2, 5);
        System.out.println("After delete: " + sb);
        // 6. Reverse - reverse the entire StringBuilder
        sb.reverse();
        System.out.println("After reverse: " + sb);
        // 7. CharAt - get character at a specific index
        char ch = sb.charAt(2);
        System.out.println("Character at index 2: " + ch);
        // 8. SetCharAt - set character at a specific index
        sb.setCharAt(0, 'X');
        System.out.println("After setCharAt: " + sb);
        // 9. Length and Capacity
        int length = sb.length();
        int capacity = sb.capacity();
        System.out.println("Length: " + length + ", Capacity: " + capacity);
        // 10. Substring - get substring (start inclusive, end exclusive)
        String sub = sb.substring(1, 4);
        System.out.println("Substring(1,4): " + sub);
        // 11. EnsureCapacity - make sure capacity is at least a certain value
        sb.ensureCapacity(50);
        System.out.println("Capacity after ensureCapacity(50): " + sb.capacity());
    }
}


//BINARY TREES:
/* Q1.Binary search-Iterative : Given a sorted array of integers and multiple query values.
Find the index of each query in the array using iterative binary search.
If a query is not present, return -1 for that query.*/

class BeingZero{
    public List<Integer> findIndexOfElement(List<Integer> array, List<Integer> queries){
        List<Integer> resultIndices = new ArrayList<>();
        for (int target : queries) {
            int left = 0;                    // Starting index of the search range
            int right = array.size() - 1;    // Ending index of the search range
            int foundIndex = -1;             // Stores index if target is found
            // Binary Search loop
            while (left <= right) {
                // Calculate middle index safely
                int mid = left + (right - left) / 2;
                // If target is found at mid
                if (array.get(mid) == target) {
                    foundIndex = mid;
                    break;
                }
                // If target is greater, search right half
                else if (array.get(mid) < target) {
                    left = mid + 1;
                }
                // If target is smaller, search left half
                else {
                    right = mid - 1;
                }
            }
            // Add result for current query
            resultIndices.add(foundIndex);
        }
        // Return list of indices for all queries
        return resultIndices;
    }
}





/* Q2.Binary search-Recursive : Given a sorted array of integers, 
search for a given key using recursive binary search and return its index.
If the key is not present, return -1.*/


class BeingZero {
    public int binarySearchRecursion(int[] array, int target) {
        return recursiveSearch(array, target, 0, array.length - 1);
    }
    // Helper function that performs recursive binary search
    public int recursiveSearch(int[] array, int target, int left, int right) {
        // Base case: if search range is invalid, element is not found
        if (left > right) {
            return -1;
        }
        // Find the middle index
        int mid = left + (right - left) / 2;
        // If target is found at mid, return its index
        if (array[mid] == target) {
            return mid;
        }
        // If target is smaller, search in the left half
        else if (array[mid] > target) {
            return recursiveSearch(array, target, left, mid - 1);
        }
        // If target is greater, search in the right half
        else {
            return recursiveSearch(array, target, mid + 1, right);
        }
    }
}





/* Q3.Search Insert Position : Given a sorted array of distinct integers and a target value, 
return the index if the target exists.If not, return the index where it should be inserted 
to keep the array sorted (in O(log n) time).*/

class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int testCases = scanner.nextInt();
        for (int t = 0; t < testCases; t++) {
            int size = scanner.nextInt();
            int target = scanner.nextInt();
            // Input sorted array
            int[] array = new int[size];
            for (int i = 0; i < size; i++) {
                array[i] = scanner.nextInt();
            }
            // Print the result for current test case
            System.out.println(searchInsertPosition(array, target));
        }
        scanner.close();
    }
    // Function to find the index of target or insertion position
    public static int searchInsertPosition(int[] array, int target) {
        int left = 0;                   // Left boundary
        int right = array.length - 1;   // Right boundary
        // Binary search loop
        while (left <= right) {
            // Find middle index
            int mid = left + (right - left) / 2;
            // If target is found, return index
            if (array[mid] == target) {
                return mid;
            }
            // If target is greater, move to right half
            else if (array[mid] < target) {
                left = mid + 1;
            }
            // If target is smaller, move to left half
            else {
                right = mid - 1;
            }
        }
        // If not found, left is the correct insertion position
        return left;
    }
}





/* Q4.Search Everywhere : Given an array A of N numbers and Q queries, 
for each query value X, print "found" if X exists in the array, otherwise print "not found".*/

class BeingZero {
    public List<String> solve(int[] array, int[] queries) {
        List<String> result = new ArrayList<>();
        // Sort the array to apply binary search
        Arrays.sort(array);
        for (int target : queries) {
            // Check if target exists using binary search
            if (binarySearch(array, target)) {
                result.add("found");
            } else {
                result.add("not found");
            }
        }
        return result;
    }
    // Helper function to perform iterative binary search
    private boolean binarySearch(int[] array, int target) {
        int left = 0;                     // Start index
        int right = array.length - 1;     // End index
        // Binary search loop
        while (left <= right) {
            // Calculate mid index
            int mid = left + (right - left) / 2;
            // If target is found
            if (array[mid] == target) {
                return true;
            }
            // If target is greater, move right
            else if (array[mid] < target) {
                left = mid + 1;
            }
            // If target is smaller, move left
            else {
                right = mid - 1;
            }
        }
        // Target not found
        return false;
    }
}





/*Q5.Valid Perfect Square : Given a positive integer num, return true if it is a perfect square, 
otherwise return false.You must not use built-in functions like sqrt. */

class BeingZero {
    public boolean validPerfectSquare(int n) {
        // Perfect squares are always positive
        if (n < 1) {
            return false;
        }
        int left = 1;          // Smallest possible square root
        int right = n;         // Largest possible square root (safe upper bound)
        // Binary search to find an integer whose square is n
        while (left <= right) {
            // Find middle value
            int mid = left + (right - left) / 2;
            // Use long to avoid overflow when squaring
            long square = (long) mid * mid;
            // If square matches n, it is a perfect square
            if (square == n) {
                return true;
            }
            // If square is greater than n, search left half
            else if (square > n) {
                right = mid - 1;
            }
            // If square is smaller than n, search right half
            else {
                left = mid + 1;
            }
        }
        // No integer square found
        return false;
    }
}




/* Q6. Median of Two Sorted Array : You are given two sorted arrays nums1 and nums2.The total 
number of elements (m + n) is always odd.Return the median of the combined sorted array without 
using sort. */

class BeingZero {
    public int solve(int[] nums1, int[] nums2) {
        int n1 = nums1.length;      // Size of first array
        int n2 = nums2.length;      // Size of second array
        // Median index in the merged sorted order
        int medianIndex = (n1 + n2) / 2;
        int i = 0;                  // Pointer for nums1
        int j = 0;                  // Pointer for nums2
        int count = 0;              // Tracks position in merged order
        int current = 0;            // Stores current merged element
        // Merge both arrays until one of them is exhausted
        while (i < n1 && j < n2) {
            // Pick smaller element from both arrays
            if (nums1[i] < nums2[j]) {
                current = nums1[i];
                i++;
            } else {
                current = nums2[j];
                j++;
            }
            // If we reached the median position, return the value
            if (count == medianIndex) {
                return current;
            }
            count++;   // Move to next merged position
        }
        // If elements are remaining in nums1
        while (i < n1) {
            current = nums1[i];

            if (count == medianIndex) {
                return current;
            }

            i++;
            count++;
        }
        // If elements are remaining in nums2
        while (j < n2) {
            current = nums2[j];

            if (count == medianIndex) {
                return current;
            }

            j++;
            count++;
        }
        // This line will never execute for valid inputs
        return -1;
    }
}






/*Q7.Count Number of Zeros : Given a sorted binary array (containing only 0s and 1s), find the 
number of zeros in the array.A linear-time solution is not allowed, so we must use binary search.*/

class BeingZero {
    public int solve(int[] array) {
        int n = array.length;
        int left = 0;
        int right = n - 1;
        int firstZeroIndex = -1;
        // Binary search to find the first occurrence of 0
        while (left <= right) {
            int mid = left + (right - left) / 2;
            if (array[mid] == 0) {
                firstZeroIndex = mid;     // Possible first zero
                right = mid - 1;          // Search left side
            } else {
                left = mid + 1;           // Search right side
            }
        }
        // If no zero is found
        if (firstZeroIndex == -1) {
            return 0;
        }
        // Number of zeros = total length - index of first zero
        return n - firstZeroIndex;
    }
}





/* Q8.Finding The Floor : Given an array and multiple queries, for each query value X, find the floor 
of X in the array.The floor is the largest element ≤ X. If no such element exists, return -1.*/

class BeingZero {
    public List<Integer> findFloor(List<Integer> arr, List<Integer> queries) {
        List<Integer> result = new ArrayList<>();
        // Sort the array since binary search requires sorted data
        Collections.sort(arr);
        // Process each query
        for (int query : queries) {
            result.add(findFloorValue(arr, query));
        }
        return result;
    }
    // Helper function to find floor of a single query using binary search
    public static int findFloorValue(List<Integer> arr, int target) {
        int left = 0;
        int right = arr.size() - 1;
        int floorValue = -1;   // Stores the best floor value found so far
        while (left <= right) {
            int mid = left + (right - left) / 2;
            // If current value is <= target, it can be a floor
            if (arr.get(mid) <= target) {
                floorValue = arr.get(mid);  // Update floor
                left = mid + 1;             // Try to find a larger valid floor
            }
            // If current value is greater, move left
            else {
                right = mid - 1;
            }
        }
        return floorValue;
    }
}





/* Q9. Index of Peak Element : A peak element is an element that is strictly greater than 
its neighbors.Given a 0-indexed array, return the index of any peak element.
Assume elements outside the array are −∞ and solve in O(log n) time.*/

class BeingZero {
    public int solve(int[] nums) {
        int n = nums.length;
        // Edge case: only one element
        if (n == 1) {
            return 0;
        }
        // Check boundary elements
        if (nums[0] > nums[1]) {
            return 0;
        }
        if (nums[n - 1] > nums[n - 2]) {
            return n - 1;
        }
        // Binary search on the remaining range
        int left = 1;
        int right = n - 2;
        while (left <= right) {
            int mid = left + (right - left) / 2;
            // If mid is a peak
            if (nums[mid] > nums[mid - 1] && nums[mid] > nums[mid + 1]) {
                return mid;
            }
            // If left neighbor is greater, peak lies on left side
            else if (nums[mid - 1] > nums[mid]) {
                right = mid - 1;
            }
            // Otherwise, peak lies on right side
            else {
                left = mid + 1;
            }
        }
        // Control should never reach here for valid input
        return -1;
    }
}





/* Q10. Square Root : Given a positive number N (which is always a perfect square), 
find and print its square root without using built-in functions. */

class Main {    
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        while (t-- > 0) {
            long n = sc.nextLong();
            System.out.println(squareRoot(n));
        }
        sc.close();
    }
    // Function to find square root using binary search
    public static long squareRoot(long n) {
        long left = 0;
        long right = n;
        long answer = 0;
        // Binary search to find exact square root
        while (left <= right) {
            long mid = left + (right - left) / 2;
            // To avoid overflow, compare mid <= n / mid
            if (mid <= n / mid) {
                answer = mid;
                left = mid + 1;
            } else {
                right = mid - 1;
            }
        }
        return answer;
    }
}





/* Q11. Matrix Search II : Given a row-wise and fully sorted matrix, find the position (row, col) 
of a target value X using an efficient search.If X is not present, return an empty list.
You must do this in O(log(R×C)) time.*/

class BeingZero {
    public List<Integer> solve(List<List<Integer>> mat, int x) {
        List<Integer> result = new ArrayList<>();
        int rows = mat.size();
        if (rows == 0) return result;
        int cols = mat.get(0).size();
        int left = 0;
        int right = rows * cols - 1;
        // Binary search on the virtual 1D array
        while (left <= right) {
            int mid = left + (right - left) / 2;
            // Convert 1D index to 2D indices
            int rowIndex = mid / cols;
            int colIndex = mid % cols;
            int midValue = mat.get(rowIndex).get(colIndex);
            // If target found
            if (midValue == x) {
                result.add(rowIndex);
                result.add(colIndex);
                return result;
            }
            // If target is greater, search right half
            else if (midValue < x) {
                left = mid + 1;
            }
            // If target is smaller, search left half
            else {
                right = mid - 1;
            }
        }
        // Target not found
        return result;
    }
}





/* Q12. Rectangles in a Square : You are given N identical rectangles of size W × H.
Without rotating them, find the minimum side length of a square that can fit all N rectangles. */

class BeingZero {
    public long rectangle(int w, int h, int n) {
        long left = 0;                          // Minimum possible side length
        long right = (long) Math.max(w, h) * n; // Safe upper bound for square side
        long answer = right;                    // Stores minimum valid square side
        // Binary search on the side length of the square
        while (left <= right) {
            long mid = left + (right - left) / 2;
            // Check if a square of side 'mid' can fit all rectangles
            if (canFit(mid, w, h, n)) {
                answer = mid;       // Update answer if possible
                right = mid - 1;    // Try to find a smaller valid square
            } else {
                left = mid + 1;     // Increase square size
            }
        }
        return answer;
    }
    // Helper function to check if 'n' rectangles can fit in a square of side 'side'
    public static boolean canFit(long side, long w, long h, long n) {
        long rectanglesFit = (side / w) * (side / h);
        // Check if total rectangles that fit is at least n
        return rectanglesFit >= n;
    }
}





/* Q13. Rope Division : You are given n ropes of different lengths and want to cut them into k 
pieces of equal length.Find the maximum possible length of each piece (answer rounded to 6 decimal 
places). */

class BeingZero {
    public double solve(ArrayList<Integer> ropes, int n, int k) {
        int size = ropes.size();
        // Convert ArrayList to array for faster access
        double[] lengths = new double[size];
        for (int i = 0; i < size; i++) {
            lengths[i] = ropes.get(i);
        }
        double low = 0.0;                        // Minimum possible length
        double high = Collections.max(ropes);   // Maximum possible length
        double answer = 0.0;
        // Perform binary search for precision-based answer
        // Loop runs fixed number of times to ensure accuracy
        for (int i = 0; i < 100; i++) {
            // Mid represents a candidate length
            double mid = (low + high) / 2;
            // Count how many pieces of length 'mid' can be formed
            int pieces = countPieces(lengths, mid);
            // If we can form at least k pieces, try larger length
            if (pieces >= k) {
                answer = mid;
                low = mid;
            }
            // Otherwise, reduce the length
            else {
                high = mid;
            }
        }
        return answer;
    }
    // Helper function to count how many pieces of length 'len' can be cut
    public static int countPieces(double[] lengths, double len) {
        int count = 0;
        // For each rope, count how many pieces of length 'len' it contributes
        for (double rope : lengths) {
            count += (int) (rope / len);
        }
        return count;
    }
}





/* Q14. Vamsi and Chocolates : Vamsi has N boxes of chocolates and H hours.He eats K chocolates per 
hour from one box.Find the minimum integer K such that he can finish all chocolates within H hours.*/

class BeingZero {
    public int minEatingSpeed(int[] chocolates, int hours) {
        int low = 1;                  // Minimum possible eating speed
        int high = 1000000000;        // Maximum possible eating speed (safe upper bound)
        // Binary search on eating speed K
        while (low <= high) {
            int mid = low + (high - low) / 2;   // Candidate eating speed
            // Calculate hours needed if eating speed is mid
            int requiredHours = calculateHours(chocolates, mid);
            // If he can finish within given hours, try smaller speed
            if (requiredHours <= hours) {
                high = mid - 1;
            }
            // Otherwise, speed is too slow → increase speed
            else {
                low = mid + 1;
            }
        }
        // Low will be the minimum valid eating speed
        return low;
    }
    // Helper function to calculate total hours needed for a given eating speed K
    public static int calculateHours(int[] chocolates, int k) {
        int totalHours = 0;
        // For each box of chocolates
        for (int i = 0; i < chocolates.length; i++) {
            // Each box takes ceil(chocolates[i] / k) hours
            totalHours += Math.ceil(chocolates[i] / (k * 1.0));
        }
        return totalHours;
    }
}





/* Q15. Machines and Machines and Machines!!! : You have n machines, each taking a certain time to 
produce one product.All machines work simultaneously.
Find the minimum time required to produce t products in total. */

class BeingZero {
    public long machines(int n, int t, int[] times) {
        // Sort machine times so that the fastest machine is at index 0
        // (used to set an efficient upper bound)
        java.util.Arrays.sort(times);
        long low = 1;                         // Minimum possible time
        long high = (long) times[0] * t;      // Maximum time if fastest machine makes all products
        long answer = high;                   // Stores minimum valid time
        // Binary search on time
        while (low <= high) {
            long mid = low + (high - low) / 2;   // Candidate time
            // Check if it's possible to make at least t products in 'mid' time
            if (canProduce(times, t, mid)) {
                answer = mid;        // Update answer
                high = mid - 1;      // Try to find smaller time
            } else {
                low = mid + 1;       // Increase time
            }
        }
        return answer;
    }
    // Helper function to check feasibility for a given time
    public static boolean canProduce(int[] times, int t, long timeLimit) {
        long totalProducts = 0;
        // Each machine contributes (timeLimit / machineTime) products
        for (int machineTime : times) {
            totalProducts += timeLimit / machineTime;
            // Early exit to avoid overflow and unnecessary computation
            if (totalProducts >= t) {
                return true;
            }
        }
        return totalProducts >= t;
    }
}





/* Q16. City Building : You are given an array a[] where each element represents the height of a 
building.You have X extra floors that can be used to increase shorter buildings.
Choose the maximum possible height h such that all buildings can be raised to at least h using 
at most X floors. */

class BeingZero {
    public int solve(int[] buildings, int maxFloors) {
        long low = 1;                 // Minimum possible height
        long high = (long) 2e9;       // Maximum possible height (safe upper bound)
        // Binary search to find the maximum valid height
        while (low < high) {
            // Take upper mid to avoid infinite loop
            long mid = low + (high - low + 1) / 2;
            // Check if we can raise all buildings to height 'mid'
            // using at most maxFloors floors
            if (canBuild(buildings, maxFloors, mid)) {
                low = mid;            // mid is possible, try higher
            } else {
                high = mid - 1;       // mid is not possible, try lower
            }
        }
        // 'low' will contain the maximum achievable height
        return (int) low;
    }
    // Helper function to check feasibility of height 'targetHeight'
    public static boolean canBuild(int[] buildings, int maxFloors, long targetHeight) {
        long floorsNeeded = 0;        // Total extra floors required
        // Traverse all buildings
        for (int height : buildings) {
            // If building is shorter than target height,
            // add required floors
            if (height < targetHeight) {
                floorsNeeded += (targetHeight - height);
                // If required floors exceed available floors,
                // target height is not possible
                if (floorsNeeded > maxFloors) {
                    return false;
                }
            }
        }
        // Target height can be achieved within available floors
        return true;
    }
}





/* Q17. Committee Formation : You are given N groups of students, where a[i] is the number of 
students in the i-th group.Each committee must have exactly K students, and no two students in a 
committee can come from the same group.Find the maximum number of committees that can be formed.*/

class BeingZero {
    public long solve(int[] groups, int k) {
        long low = 0;          // Minimum possible number of committees
        long sum = 0;
        // Sum of all students
        for (int students : groups) {
            sum += students;
        }
        // Maximum committees possible cannot exceed total students / k
        long high = sum / k + 1;
        // Binary search to find maximum valid committees
        while (high - low > 1) {
            long mid = (low + high) / 2;   // Candidate number of committees
            // Check if 'mid' committees can be formed
            if (canForm(groups, k, mid)) {
                low = mid;     // mid is possible, try to increase
            } else {
                high = mid;    // mid is not possible, reduce
            }
        }
        return low;
    }
    // Helper function to check feasibility of forming 'm' committees
    public static boolean canForm(int[] groups, int k, long m) {
        long totalStudentsUsed = 0;
        // From each group, we can take at most 'm' students
        // because a group can contribute at most one student per committee
        for (int groupSize : groups) {
            totalStudentsUsed += Math.min(groupSize, m);
        }
        // To form 'm' committees, we need exactly m * k students
        return totalStudentsUsed >= m * k;
    }
}





/* Q18. Allocate Books : You are given an array where each element represents the number of pages in a book.
You must allocate these books to B students such that:
    Each student gets at least one book
    Books are assigned in contiguous order
    The maximum pages assigned to any student is minimized
Return this minimum possible maximum number of pages.
If allocation is not possible, return -1.*/

class BeingZero {
    public int findMinPages(int[] books, int totalBooks, int studentsCount) {
        // If students are more than books, allocation is impossible
        if (totalBooks < studentsCount) {
            return -1;
        }
        int minPages = 0;   // Lower bound (max pages in a single book)
        int maxPages = 0;   // Upper bound (sum of all pages)
        // Initialize search boundaries
        for (int pages : books) {
            minPages = Math.max(minPages, pages);
            maxPages += pages;
        }
        int answer = -1;
        // Binary search to minimize the maximum pages
        while (minPages <= maxPages) {
            int midPages = minPages + (maxPages - minPages) / 2;
            // Check if allocation is possible with midPages limit
            if (isAllocationPossible(books, studentsCount, midPages)) {
                answer = midPages;        // Valid answer found
                maxPages = midPages - 1;  // Try smaller maximum
            } else {
                minPages = midPages + 1;  // Increase maximum pages
            }
        }
        return answer;
    }
    // Helper function to check if books can be allocated
    // such that no student gets more than maxAllowedPages
    public boolean isAllocationPossible(int[] books, int studentsCount, int maxAllowedPages) {
        int studentsUsed = 1;   // Start with first student
        int pagesAllocated = 0;
        for (int pages : books) {
            // If a single book exceeds maxAllowedPages, allocation fails
            if (pages > maxAllowedPages) {
                return false;
            }
            // If current student exceeds limit, assign book to next student
            if (pagesAllocated + pages > maxAllowedPages) {
                studentsUsed++;
                pagesAllocated = pages;
                // If students exceed available count, allocation fails
                if (studentsUsed > studentsCount) {
                    return false;
                }
            } else {
                // Add pages to current student
                pagesAllocated += pages;
            }
        }
        return true;
    }
}





/* Q19. K-th Number in the Union Ranges : You are given N integer ranges [𝐿𝑖,𝑅𝑖][Li,Ri].
Imagine writing all numbers from all ranges into one big array:
If a number appears in multiple ranges, it appears multiple times
The array is then sorted
You must find the K-th element (0-indexed) in this sorted array
It is guaranteed that the K-th element exists.*/

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int testCases = sc.nextInt();
        while (testCases-- > 0) {
            int numberOfRanges = sc.nextInt();
            long k = sc.nextLong(); // 0-based index
            long[][] ranges = new long[numberOfRanges][2];
            for (int i = 0; i < numberOfRanges; i++) {
                ranges[i][0] = sc.nextLong(); // L
                ranges[i][1] = sc.nextLong(); // R
            }
            System.out.println(findKthNumber(ranges, k));
        }
        sc.close();
    }

    public static long findKthNumber(long[][] ranges, long k) {
        long minValue = Long.MAX_VALUE; // smallest possible number
        long maxValue = Long.MIN_VALUE; // largest possible number
        // Step 1: Find search boundaries
        for (long[] range : ranges) {
            minValue = Math.min(minValue, range[0]);
            maxValue = Math.max(maxValue, range[1]);
        }
        long left = minValue;
        long right = maxValue;
        long answer = -1;
        // Step 2: Binary search on value range
        while (left <= right) {
            long mid = left + (right - left) / 2;
            // Step 3: Count how many numbers ≤ mid exist
            long count = 0;
            for (long[] range : ranges) {
                long start = range[0];
                long end = range[1];
                // Count contribution from this range
                if (mid >= start) {
                    count += Math.min(end, mid) - start + 1;
                }
            }
            // Step 4: Adjust search space
            if (count > k) {
                answer = mid;      // mid is a valid candidate
                right = mid - 1;   // try smaller values
            } else {
                left = mid + 1;    // need larger values
            }
        }
        return answer;
    }

}





/* Q20. Weird Machines : You are given N machines working in parallel.
Each machine produces items daily in a repeating pattern:
    Machine i produces ((day−1)modi)+1 items on a given day.
All machines start on Day 1.
Your task is to find the minimum number of days required to produce at least X items in total. */

class BeingZero {
    public long weirdMachine(int numberOfMachines, long requiredItems) {
        long lowDay = 1;              // minimum possible day
        long highDay = requiredItems; // safe upper bound
        long answer = requiredItems;
        // Binary search on number of days
        while (lowDay <= highDay) {
            long midDay = lowDay + (highDay - lowDay) / 2;
            // Check how many items are produced in midDay days
            if (canProduce(midDay, numberOfMachines, requiredItems)) {
                answer = midDay;        // midDay is a valid answer
                highDay = midDay - 1;   // try to find smaller day
            } else {
                lowDay = midDay + 1;    // need more days
            }
        }
        return answer;
    }
    // Helper function to check if we can produce requiredItems in given days
    private boolean canProduce(long days, int numberOfMachines, long requiredItems) {
        long totalItemsProduced = 0;
        // Calculate production for each machine
        for (int machineIndex = 1; machineIndex <= numberOfMachines; machineIndex++) {

            // One full cycle length for this machine
            long cycleLength = machineIndex;

            // Total items produced in one full cycle
            long itemsPerCycle = (cycleLength * (cycleLength + 1)) / 2;

            // Number of complete cycles
            long fullCycles = days / cycleLength;

            // Remaining days after full cycles
            long remainingDays = days % cycleLength;

            // Total production from this machine
            totalItemsProduced += fullCycles * itemsPerCycle;
            totalItemsProduced += (remainingDays * (remainingDays + 1)) / 2;

            // Early stopping to avoid overflow
            if (totalItemsProduced >= requiredItems) {
                return true;
            }
        }
        return totalItemsProduced >= requiredItems;
    }
}




/* 21.Rotated Sorted Array : You are given a sorted array that has been rotated at an 
unknown pivot and a target value.
Your task is to find the index of the target in the array using O(log N) time complexity.
If the target does not exist, return -1. */

class BinaryZero {
    public int findIndexInSortedRotated(int[] arr, int target) {
        int left = 0;                    // Starting index
        int right = arr.length - 1;      // Ending index
        // Binary Search loop
        while (left <= right) {
            int mid = left + (right - left) / 2; // Prevents overflow
            // If target found at mid
            if (arr[mid] == target) {
                return mid;
            }
            // Check if left half is sorted
            if (arr[left] <= arr[mid]) {
                // Target lies in the sorted left half
                if (target >= arr[left] && target < arr[mid]) {
                    right = mid - 1;
                } 
                // Target lies in the right half
                else {
                    left = mid + 1;
                }
            } 
            // Otherwise, right half is sorted
            else {
                // Target lies in the sorted right half
                if (target > arr[mid] && target <= arr[right]) {
                    left = mid + 1;
                } 
                // Target lies in the left half
                else {
                    right = mid - 1;
                }
            }
        }
        // Target not found
        return -1;
    }
}

//Set, Map Operations:

//MAP
//Write a Java program using Map to store key–value pairs and search for a given key.
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

class MapKeySearch {

    public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
        Map<Integer, String> map = new HashMap<>();
        map.put(1, "A");
        map.put(2, "B");
        map.put(3, "Ch");
        map.put(4, "D");
        System.out.println("Student Map: " + map);
        System.out.print("Enter the key to search: ");
        int key = sc.nextInt();

        // Check if the key exists in the map
        if (map.containsKey(key)) {
            // If key exists, print the value
            System.out.println("Key found!");
            System.out.println("Value: " + map.get(key));
        } else {
            // If key does not exist
            System.out.println("Key not found.");
        }

    }
}


//Frind duplicate values in an array  using Map.
import java.util.*;;

class DuplicateValuesCounter {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] array = new int[n];

        for (int i = 0; i < n; i++) {
            array[i] = sc.nextInt();
        }
        HashMap<Integer, Integer> countMap = new HashMap<>();
        // Count frequency of each element
        for (int num : array) {
            if (countMap.containsKey(num)) {
                // If element already exists, increment
                countMap.put(num, countMap.get(num) + 1);
            } else {
                // First occurrence
                countMap.put(num, 1);
            }
        }
        // Print elements whose count is >1
        for (int key : countMap.keySet()) {
            if (countMap.get(key) > 1) {
                System.out.println(key + " occurs " + countMap.get(key) + " times.");
            }
        }
    }
}




//Subarrays:

class BeingZero {
    public long solve(int a[], int n, int x) {
        long ans = 0;
        long sum = 0;
        Map<Long, Integer> m = new HashMap<>();
        // Prefix sum frequency map to count subarrays with sum = x
        m.put(0L, 1);
        for (int i = 0; i < n; i++) {
            sum += a[i];

            if (m.containsKey(sum - x))
                ans += m.get(sum - x);

            m.put(sum, m.getOrDefault(sum, 0) + 1);
        }
        return ans;
    }
}


// count total subarrays whose sum=0 or k using formula count(<=k) - count(<=(k-1)) = count==k
class BeingZero {
    private long countAtMost(int[] a, int n, int k) {
        long sum = 0, cnt = 0;
        int s = 0;
        for (int e = 0; e < n; e++) {
            sum += a[e];
            while (sum > k) {
                sum -= a[s];
                s++;
            }
            cnt += e - s + 1;
        }
        return cnt;
    }
    public long solve(int[] a, int n, int k) {
        // count(sum == k) = count(sum ≤ k) - count(sum ≤ k-1)
        return countAtMost(a, n, k) - countAtMost(a, n, k - 1);
    }
}


// length of subarray whose sum = 0 or k map, prefix sum
import java.util.*;

class BeingZero {
    public int longestSubarraySumK(List<Integer> a, int n, int k) {
        Map<Integer, Integer> m = new HashMap<>();
        int len = 0, sum = 0;
        // Prefix sum map to track longest subarray with sum = k
        for (int i = 0; i < n; i++) {
            sum += a.get(i);
            if (sum == k)
                len = i + 1;
            if (m.containsKey(sum - k)) {
                int l = i - m.get(sum - k);
                len = Math.max(len, l);
            }
            if (!m.containsKey(sum))
                m.put(sum, i);
        }
        return len;
    }
}


// length of longest substring with k distinct characters
import java.util.*;
import java.io.*;
class BeingZero {
    public int solve(String s, int k) {
        int ans = 0;
        Map<Character, Integer> m = new HashMap<>();
        int st = 0;
        // Sliding window to find longest substring with at most k distinct characters
        for (int e = 0; e < s.length(); e++) {
            char ch = s.charAt(e);
            m.put(ch, 1 + m.getOrDefault(ch, 0));
            while (m.size() > k) {
                char cs = s.charAt(st);
                int f = m.get(cs);
                m.put(cs, f - 1);
                if (m.get(cs) == 0) m.remove(cs);
                st++;
            }
            ans = Math.max(ans, e - st + 1);
        }
        return ans;
    }
}


// count segments with small sum
class BeingZero {
    public long countSegmentsWithBigSum(List<Integer> a, long k) {
        long sum = 0;
        int s = 0;
        int n = a.size();
        int count = 0;
        // Two-pointer window to count subarrays with sum ≥ k
        for (int e = 0; e < n; e++) {
            sum += a.get(e);
            while (sum <= k) {
                count += n - e;
                sum -= a.get(s);
                s++;
            }
        }
        return count;
    }
}



// length of segment with small sum
class BeingZero {
    public int segmentWithSmallSum(int[] a, int s) {
        int i = 0, j = 0;
        int n = a.length;
        int sum = 0, max = 0;
        // Sliding window to find maximum length subarray with sum ≤ s
        while (i < n) {
            sum += a[i];
            while (sum > s) {
                sum -= a[j];
                j++;
            }
            max = Math.max(max, i - j + 1);
            i++;
        }
        return max;
    }
}



// count segments with big sum
class BeingZero {
    public long countSegmentsWithBigSum(List<Integer> a, long k) {
        long sum = 0;
        int s = 0;
        int n = a.size();
        int count = 0;
        // Two-pointer window to count subarrays with sum ≥ k
        for (int e = 0; e < n; e++) {
            sum += a.get(e);
            while (sum >= k) {
                count += n - e;
                sum -= a.get(s);
                s++;
            }
        }
        return count;
    }
}



// length of segment with big sum
class BeingZero {
    public int segmentWithSmallSum(int[] a, int s) {
        int i = 0, j = 0;
        int n = a.length;
        int sum = 0, max = 0;
        // Sliding window to find maximum length subarray with sum ≤ s
        while (i < n) {
            sum += a[i];
            while (sum < s) {
                sum -= a[j];
                j++;
            }
            max = Math.max(max, i - j + 1);
            i++;
        }
        return max;
    }
}



// union of wo arrays
import java.util.*;
import java.io.*;

class BeingZero {
    public List<Integer> unionOfTwoArrays(List<Integer> a, List<Integer> b) {
        int i = 0, j = 0;
        int n = a.size(), m = b.size();
        List<Integer> ans = new ArrayList<>();
        // Merge both sorted lists while avoiding duplicates
        while (i < n && j < m) {
            if (a.get(i) < b.get(j)) {
                if (ans.size() == 0 || !ans.get(ans.size() - 1).equals(a.get(i)))
                    ans.add(a.get(i));
                i++;
            } else {
                if (ans.size() == 0 || !ans.get(ans.size() - 1).equals(b.get(j)))
                    ans.add(b.get(j));
                j++;
            }
        }
        while (i < n) {
            if (ans.size() == 0 || !ans.get(ans.size() - 1).equals(a.get(i)))
                ans.add(a.get(i));
            i++;
        }
        while (j < m) {
            if (ans.size() == 0 || !ans.get(ans.size() - 1).equals(b.get(j)))
                ans.add(b.get(j));
            j++;
        }
        return ans;
    }
}



// intersection of two arrays
import java.util.*;
import java.io.*;

class BeingZero {
    public List<Integer> intersectionOfTwoArrays(List<Integer> a, List<Integer> b) {
        List<Integer> ans = new ArrayList<>();
        int n = a.size(), m = b.size();
        int i = 0, j = 0;
        // Two-pointer traversal to collect common elements without duplicates
        while (i < n && j < m) {
            if (a.get(i).equals(b.get(j))) {
                if (ans.size() == 0 || !ans.get(ans.size() - 1).equals(a.get(i)))
                    ans.add(a.get(i));
                i++;
                j++;
            } else if (a.get(i) < b.get(j)) {
                i++;
            } else {
                j++;
            }
        }
        return ans;
    }
}



// sorted array of squares
class BeingZero {
    public long[] solve(int a[], int n) {
        long[] arr = new long[n];
        int i = 0, j = n - 1, k = n - 1;
        // Compare squares from both ends and fill from back
        while (i <= j) {
            long left = a[i] * a[i];
            long right = a[j] * a[j];
            if (left >= right) {
                arr[k--] = left;
                i++;
            } else {
                arr[k--] = right;
                j--;
            }
        }
        return arr;
    }
}



// min sum of each window of length k
int minWindowSum(int[] a, int n, int k) {
    // Sliding window to find minimum sum of any subarray of size k
    int sum = 0, min = Integer.MAX_VALUE;
    for (int i = 0; i < n; i++) {
        sum += a[i];
        if (i >= k) sum -= a[i - k];
        if (i >= k - 1) min = Math.min(min, sum);
    }
    return min;
}


// max sum of each window of length k
int maxWindowSum(int[] a, int n, int k) {
    // Sliding window to find maximum sum of any subarray of size k
    int sum = 0, max = Integer.MIN_VALUE;
    for (int i = 0; i < n; i++) {
        sum += a[i];
        if (i >= k) sum -= a[i - k];
        if (i >= k - 1) max = Math.max(max, sum);
    }
    return max;
}



// unique sum of each window of length k
int[] uniqueWindowSum(int[] a, int n, int k) {
    // Maintain frequency map to compute sum of distinct elements in each window
    int[] res = new int[n - k + 1];
    Map<Integer, Integer> m = new HashMap<>();
    int sum = 0;

    for (int i = 0; i < n; i++) {
        m.put(a[i], m.getOrDefault(a[i], 0) + 1);
        if (m.get(a[i]) == 1) sum += a[i];

        if (i >= k) {
            m.put(a[i - k], m.get(a[i - k]) - 1);
            if (m.get(a[i - k]) == 0) {
                m.remove(a[i - k]);
                sum -= a[i - k];
            }
        }
        if (i >= k - 1) res[i - k + 1] = sum;
    }
    return res;
}

//Linked List:

//Merge Two Sorted Lists
//Merge two sorted singly linked lists into one sorted linked list by reusing and rearranging the existing nodes (no new nodes created).

class SLLNode {
    int data;          
    SLLNode next;  

    SLLNode(int d) {
        data = d;
        next = null;
    }
}

class Main {

    public SLLNode mergeTwoSortedLists(SLLNode a, SLLNode b) {

        if (a == null)
            return b;

        if (b == null)
            return a;

        if (a.data <= b.data) {
            a.next = mergeTwoSortedLists(a.next, b);

            return a;
        }
        else {
            // If data of list 'b' is smaller. Recursively merge 'a' with remaining part of 'b'
            b.next = mergeTwoSortedLists(a, b.next);

            // Return current node of list 'b'
            return b;
        }
    }
}



// Palindromic List
//Given a singly linked list, check whether it is palindromic list or not.
class SLLNode {
    int data;        
    SLLNode next;      

    SLLNode(int d) {
        data = d;
        next = null;
    }
}
class Main {
    public boolean isPalindromic(SLLNode h) {
        if (h == null)
            return true;
        SLLNode m = midNode(h);
        // Reverse the second half of the list
        SLLNode h1 = reverse(m);
        // Compare first half and reversed second half
        while (h1 != null) {
            if (h.data != h1.data) {
                return false; // mismatch found
            }
            h = h.next;
            h1 = h1.next;
        }
        
        return true;
    
    public SLLNode midNode(SLLNode head) {
        SLLNode f = head; 
        SLLNode s = head; 
        while (f != null && f.next != null) {
            f = f.next.next;
            s = s.next;
        }
        return s;
    }
    public SLLNode reverse(SLLNode head) {
        SLLNode prev = null;
        SLLNode curr = head;
        SLLNode n = null;
        while (curr != null) {
            n = curr.next;
            curr.next = prev;
            prev = curr;
            curr = n;
        }
        return prev;
    }
}
}


//LIST CYCLE
//Given a singly linked list, check if it contains a loop and return the node where the loop starts; if there is no loop, return null.

class SLLNode {
    int data;          
    SLLNode next;      
    SLLNode(int d) {
        data = d;
        next = null;
    }
}
class Main{

    public SLLNode cycleStartNode(SLLNode a) {
        if (a == null)
            return null;

        SLLNode s = a;   
        SLLNode f = a;   

    // Detect cycle using Floyd’s Cycle Detection
        while (f != null && f.next != null) {

            s = s.next;          
            f = f.next.next;    

            // If slow and fast meet, cycle exists
            if (s == f) {

                s = a; // move slow back to head .Find the starting node of the cycle

                // Move both pointers one step at a time
                while (s != f) {
                    s = s.next;
                    f = f.next;
                }

                // Meeting point is the start of the cycle
                return s;
            }
        }

        // If no cycle is found
        return null;
    }
}



//Stack,Queue & Priority Queue:

//Stack:

//You are given an array A of size N, and for each element in the array, you need to find its Next Greater Element (NGE).
//The NGE for an element x is the first element to its right that is strictly greater than x. If no such element exists, the NGE is -1.
class NextGreaterElement {
    public int[] Solve(int arr[], int n) {
        int ans[] = new int[n]; // Stores the Next Greater Elements
        Stack<Integer> st = new Stack<>(); // Stack to track indices
        Arrays.fill(ans, -1); // Initialize NGE as -1 for all elements
        for (int i = 0; i < n; i++) {
            // Find NGE for elements in the stack
            while (!st.isEmpty() && arr[i] > arr[st.peek()]) {
                ans[st.pop()] = arr[i]; // Assign NGE and remove from stack
            }
            st.push(i); // Push current index for future comparisons
        }
        return ans;
    }
}

//Modifications for Other Variants of Next/Previous Greater/Smaller Elements:
         Type	                        Condition Change	   Iteration Order	        Modification Needed
Next Greater Element (NGE)	        arr[i] > arr[st.peek()]	     Left → Right	           Original code
Next Smaller Element (NSE)	        arr[i] < arr[st.peek()]	     Left → Right	           Change condition to <
Previous Greater Element (PGE)	    arr[i] > arr[st.peek()]	     Right → Left	           Reverse iteration (right to left)
Previous Smaller Element (PSE)	    arr[i] < arr[st.peek()]	     Right → Left	           Reverse iteration and change condition to <


//Queue:

//Reduce n to 1:

/*Given an integer N, using any of the below steps reduce it to 1.
Divide by 2 if N is divisible by 2.
Divide by 3 if N is divisible by 3.
Subtract 1 from N.
Find the minimum number of steps required to reduce N to 1.*/
import java.util.*;
class Pair {
    int num;       // Current number
    int steps;     // Number of steps taken to reach this number
    // Constructor to initialize the State
    public Pair(int num, int steps) {
        this.num = num;
        this.steps = steps;
    }
}
public class ReduceNto1 {
    public static int minStep(int n) {
        Queue<Pair> queue = new LinkedList<>();
        Set<Integer> visited = new HashSet<>();
        // Initialize the queue with the starting state (n, 0)
        queue.add(new Pair(n, 0));
        // Mark the starting number as visited
        visited.add(n);
         while (!queue.isEmpty()) {
            // Dequeue the current state
            Pair currentState = queue.poll();
            // Check if the current number is 1
            if (currentState.num == 1) {
                return currentState.steps;
            }
             if (currentState.num % 2 == 0) {
                int nextNum = currentState.num / 2;
                if (!visited.contains(nextNum)) {
                    queue.add(new Pair(nextNum, currentState.steps + 1));
                    visited.add(nextNum);
                }
            }
            if (currentState.num % 3 == 0) {
                int nextNum = currentState.num / 3;
                if (!visited.contains(nextNum)) {
                    queue.add(new Pair(nextNum, currentState.steps + 1));
                    visited.add(nextNum);
                }
            }
            int nextNum = currentState.num - 1;
            if (!visited.contains(nextNum)) {
                queue.add(new Pair(nextNum, currentState.steps + 1));
                visited.add(nextNum);
            }
        }
        return -1;
   }
}


//Level-Oreder Traversal:
class TreeNode{
    int val;
    TreeNode left,right;
    TreeNode(int d){
        val = d;
        left = right = null;
    }
}

class LevelOrderTraversal {
    public List<List<Integer>> levelOrder(TreeNode root) {
        // Stores final level-wise result
        List<List<Integer>> ans = new ArrayList<>();
        if (root == null) return ans;

        // Queue for BFS (level order traversal)
        Queue<TreeNode> q = new LinkedList<>();
        q.add(root);   // start from root

        while (!q.isEmpty()) {
            // Stores values of current level
            List<Integer> in = new ArrayList<>();
            int size = q.size();  // number of nodes in this level

            for (int i = 0; i < size; i++) {
                TreeNode curr = q.remove();
                in.add(curr.val);

                // Add children for next level
                if (curr.left != null) q.add(curr.left);
                if (curr.right != null) q.add(curr.right);
            }
            // Add current level to answer
            ans.add(in);
        }
        return ans;
    }
}


//Burn a Tree:
//This code calculates the minimum time required to burn an entire binary tree starting from a given target node.
//It first stores parent references for each node, then uses Breadth-First Search (BFS) to simulate the fire spreading to left child, right child, and parent level by level.
//The time is increased only when the fire spreads to new nodes.
import java.util.*;
class BurnATree {

    public int solve(TreeNode root, int targetValue) {

        int timeToBurn = 0;

        // Map to store: child node -> parent node
        Map<TreeNode, TreeNode> parentMap = new HashMap<>();

        // Queue for BFS traversal while building parent mapping
        Queue<TreeNode> bfsQueue = new LinkedList<>();

        if (root == null) return 0;

        bfsQueue.add(root);

        // -------- Step 1: Build parent mapping for every node --------
        while (!bfsQueue.isEmpty()) {
            TreeNode currentNode = bfsQueue.remove();

            // If left child exists, store its parent and push into queue
            if (currentNode.left != null) {
                parentMap.put(currentNode.left, currentNode);
                bfsQueue.add(currentNode.left);
            }

            // If right child exists, store its parent and push into queue
            if (currentNode.right != null) {
                parentMap.put(currentNode.right, currentNode);
                bfsQueue.add(currentNode.right);
            }
        }

        // -------- Step 2: Find the node where fire starts --------
        TreeNode fireStartNode = search(root, targetValue);

        // Set to track already burned (visited) nodes
        Set<TreeNode> visitedNodes = new HashSet<>();

        bfsQueue.add(fireStartNode);
        visitedNodes.add(fireStartNode);

        // -------- Step 3: BFS to simulate burning process --------
        while (!bfsQueue.isEmpty()) {

            int currentLevelSize = bfsQueue.size();   // nodes burning at current second
            boolean fireSpread = false;               // checks if fire spreads this second

            while (currentLevelSize-- > 0) {
                TreeNode burningNode = bfsQueue.remove();

                // 🔥 Burn parent node
                if (parentMap.containsKey(burningNode)) {
                    TreeNode parentNode = parentMap.get(burningNode);
                    if (!visitedNodes.contains(parentNode)) {
                        visitedNodes.add(parentNode);
                        bfsQueue.add(parentNode);
                        fireSpread = true;
                    }
                }

                // 🔥 Burn left child
                if (burningNode.left != null && !visitedNodes.contains(burningNode.left)) {
                    visitedNodes.add(burningNode.left);
                    bfsQueue.add(burningNode.left);
                    fireSpread = true;
                }

                // 🔥 Burn right child
                if (burningNode.right != null && !visitedNodes.contains(burningNode.right)) {
                    visitedNodes.add(burningNode.right);
                    bfsQueue.add(burningNode.right);
                    fireSpread = true;
                }
            }

            // Increase time only if at least one new node burned
            if (fireSpread) {
                timeToBurn++;
            }
        }

        return timeToBurn;
    }

    // -------- Helper function to find the target node in the tree --------
    public TreeNode search(TreeNode root, int value) {

        if (root == null) return null;

        if (root.val == value) return root;

        // Search in left subtree
        TreeNode leftResult = search(root.left, value);

        // Search in right subtree
        TreeNode rightResult = search(root.right, value);

        if (leftResult != null) return leftResult;
        if (rightResult != null) return rightResult;

        return null;
    }
}






//Prefix Sum:
//Static range sum queries:Given an array and multiple queries, find the sum of elements for each specified range efficiently.

class Main {
    public long[] staticRangeSumQueries(int[] array, int[][] queries) {

        int n = queries.length;      
        int m = array.length;        

        long[] result = new long[n]; 
        long[] prefixSum = new long[m]; 

        // Build prefix sum array
        // prefixSum[i] = sum of elements from index 0 to i
        prefixSum[0] = array[0];
        for (int index = 1; index < m; index++) {
            prefixSum[index] = prefixSum[index - 1] + array[index];
        }

        // Process each
        for (int queryIndex = 0; queryIndex < n; queryIndex++) {
            int leftIndex = queries[queryIndex][0];
            int rightIndex = queries[queryIndex][1];

            // If range starts from index 0
            if (leftIndex == 0) {
                result[queryIndex] = prefixSum[rightIndex];
            }
            // Otherwise subtract prefix sum before leftIndex
            else {
                result[queryIndex] = prefixSum[rightIndex] - prefixSum[leftIndex - 1];
            }
        }

        return result; 
    }
}


//Priority Queue:


/*Fractional Knapsack – Greedy Idea
You are given:
value[i] → profit of item
weight[i] → weight of item
capacity → maximum weight knapsack can hold
=> You can take fraction of an item.
 Greedy Rule : Always pick the item with maximum value / weight ratio first. */

class Item {
    int value;
    int weight;
    double ratio;

    Item(int v, int w) {
        value = v;
        weight = w;
        ratio = (double) v / w;
    }
}

public class FractionalKnapsack {
    public static void main(String[] args) {

        int[] value = {60, 100, 120};
        int[] weight = {10, 20, 30};
        int capacity = 50;

        // Max heap based on ratio
        PriorityQueue<Item> pq = new PriorityQueue<>(
            (a, b) -> Double.compare(b.ratio, a.ratio)
        );

        // Add all items to PQ
        for (int i = 0; i < value.length; i++) {
            pq.add(new Item(value[i], weight[i]));
        }

        double totalValue = 0.0;

        // Greedy selection
        while (capacity > 0 && !pq.isEmpty()) {
            Item current = pq.poll();

            if (current.weight <= capacity) {
                // Take full item
                capacity -= current.weight;
                totalValue += current.value;
            } else {
                // Take fraction
                double fraction = (double) capacity / current.weight;
                totalValue += current.value * fraction;
                capacity = 0;
            }
        }

        System.out.println("Maximum value = " + totalValue);
    }
}

/*This algorithm finds the minimum total cost to connect all elements into one chain by always merging the two smallest values first using a Min Priority Queue.
 Each merge cost is added back into the queue and accumulated into the total cost.
  This greedy approach guarantees the minimum overall cost. */

import java.util.*;

public class Mincostlongchain {
    public static long minCostLongChain(int[] arr) {

        long totalCost = 0;

        // Min Priority Queue to always get the smallest elements first
        PriorityQueue<Integer> minHeap = new PriorityQueue<>();

        // Insert all elements into the priority queue
        for (int value : arr) {
            minHeap.add(value);
        }

        // Continue until only one element remains
        while (minHeap.size() > 1) {

            // Remove two smallest elements
            int first = minHeap.poll();
            int second = minHeap.poll();

            int sum = first + second;

            // Add their sum back into the heap
            minHeap.add(sum);

            // Add the cost of this connection
            totalCost += sum;
        }

        return totalCost;
}
}


//Running Median:
/*=> The median of an array is the middle element after sorting; if the size is even, it is the average of the two middle elements.
=> Given a stream of integers arriving one by one in any order, we must calculate the median after each insertion.
=> The median should be printed up to one decimal place for every new number added.
=> Only the given function needs to be completed (no full program required). */
import java.util.*;

public class RunningMedian {
    public float[] solve(int A[], int n) {

        // Array to store median after each insertion
        float[] ans = new float[n];

        // Max heap -> stores smaller half of numbers
        PriorityQueue<Integer> leftMaxHeap = 
                new PriorityQueue<>((a, b) -> b - a);

        // Min heap -> stores larger half of numbers
        PriorityQueue<Integer> rightMinHeap = 
                new PriorityQueue<>();

        for (int i = 0; i < n; i++) {

            // If left heap is empty, insert first element there
            if (leftMaxHeap.isEmpty()) {
                leftMaxHeap.add(A[i]);
            }
            // If current element is greater than max of left heap,
            // then it belongs to right heap
            else if (leftMaxHeap.peek() < A[i]) {
                rightMinHeap.add(A[i]);
            }
            // Otherwise insert into left heap
            else {
                leftMaxHeap.add(A[i]);
            }

            // Balance the heaps so that size difference is not more than 1
            if (rightMinHeap.size() - leftMaxHeap.size() > 1) {
                leftMaxHeap.add(rightMinHeap.poll());
            }

            if (leftMaxHeap.size() - rightMinHeap.size() > 1) {
                rightMinHeap.add(leftMaxHeap.poll());
            }

            // If left heap has more elements, median is its top
            if (leftMaxHeap.size() > rightMinHeap.size()) {
                ans[i] = leftMaxHeap.peek();
            }
            // If right heap has more elements, median is its top
            else if (rightMinHeap.size() > leftMaxHeap.size()) {
                ans[i] = rightMinHeap.peek();
            }
            // If both heaps have equal size, median is average of both tops
            else {
                ans[i] = (leftMaxHeap.peek() + rightMinHeap.peek()) / 2.0f;
            }
        }

        return ans;   // Return array of running medians
    }
}


//Activity- Based Problem: Meeting Rooms
/*=> You are given a 2D List A (N × 2) where each entry represents a meeting’s start time and end time.
=> The goal is to find the minimum number of conference rooms needed so that no meetings overlap.
=> If one meeting ends at time t, another meeting starting at t can use the same room.
=> Meetings can be in any order and must be scheduled efficiently. */

import java.util.*;

class MeetingRooms {

    public int meetingRooms(ArrayList<ArrayList<Integer>> list) {

        // Min-heap to store end times of ongoing meetings
        PriorityQueue<Integer> pq = new PriorityQueue<>();

        // Sort meetings based on their start time
        Collections.sort(list, (x, y) -> x.get(0) - y.get(0));

        // Add end time of first meeting
        pq.add(list.get(0).get(1));

        int n = list.size();

        for (int i = 1; i < n; i++) {

            // If current meeting starts after or when
            // the earliest ending meeting finishes,
            // reuse the same room
            if (list.get(i).get(0) >= pq.peek()) {
                pq.remove();   // free the room
            }

            // Add current meeting's end time to heap
            pq.add(list.get(i).get(1));
        }

        // Size of priority queue represents minimum rooms needed
        return pq.size();
    }
}



//TREES: 

//BST Operations:

import java.util.*;

class TreeNode{
    int val;
    TreeNode left, right;
    TreeNode(int d){
      	val = d;
      	left = right = null;
    }
}

class BeingZero {
    TreeNode r = null;

    // Insert X into BST
    public void insert(int x) {
        r = insertRec(r, x);
    }

    private TreeNode insertRec(TreeNode root, int x) {
        if (root == null) return new TreeNode(x);
        if (x < root.val) root.left = insertRec(root.left, x);
        else if (x > root.val) root.right = insertRec(root.right, x);
        return root;
    }

    // Delete X from BST
    public void delete(int x) {
        r = deleteRec(r, x);
    }

    private TreeNode deleteRec(TreeNode root, int x) {
        if (root == null) return null;
        if (x < root.val) root.left = deleteRec(root.left, x);
        else if (x > root.val) root.right = deleteRec(root.right, x);
        else {
            // TreeNode with only one child or no child
            if (root.left == null) return root.right;
            else if (root.right == null) return root.left;
            // TreeNode with two children: get inorder successor
            root.val = minValue(root.right);
            root.right = deleteRec(root.right, root.val);
        }
        return root;
    }

    private int minValue(TreeNode root) {
        int minv = root.val;
        while (root.left != null) {
            root = root.left;
            minv = root.val;
        }
        return minv;
    }

    // Search X in BST
    public boolean search(int x) {
        return searchRec(r, x);
    }

    private boolean searchRec(TreeNode root, int x) {
        if (root == null) return false;
        if (root.val == x) return true;
        return x < root.val ? searchRec(root.left, x) : searchRec(root.right, x);
    }

    // Get PreOrder traversal as List
    public List<Integer> getPreOrder() {
        List<Integer> res = new ArrayList<>();
        preOrderRec(r, res);
        return res.isEmpty() ? null : res;
    }

    private void preOrderRec(TreeNode root, List<Integer> res) {
        if (root == null) return;
        res.add(root.val);
        preOrderRec(root.left, res);
        preOrderRec(root.right, res);
    }
}

//Diameter of Binary Tree:

class BeingZero{
    static int dia;
	static int diameterOfTree(TreeNode r){
        dia = 0;
        height(r);
        return dia;
	}
    public static int height(TreeNode r){
        if(r==null) return 0;
        int lh = height(r.left);
        int rh = height(r.right);
        dia = Math.max(dia,lh+rh+1);
        return Math.max(rh,lh)+1;
    }
}

//Level Order Traversal:

class BeingZero {

    // Function to return level-order traversal of a binary tree
    List<List<Integer>> solve(TreeNode root) {

        // Stores the final answer (list of levels)
        List<List<Integer>> result = new ArrayList<>();

        // If tree is empty, return empty list
        if (root == null) {
            return result;
        }

        // Queue for BFS traversal
        Queue<TreeNode> queue = new LinkedList<>();
        queue.add(root);

        // Continue until all levels are processed
        while (!queue.isEmpty()) {

            // List to store current level nodes
            List<Integer> currentLevel = new ArrayList<>();

            // Number of nodes at the current level
            int levelSize = queue.size();

            // Process all nodes of the current level
            for (int i = 0; i < levelSize; i++) {

                // Remove front node from queue
                TreeNode currentNode = queue.remove();

                // Add node value to current level list
                currentLevel.add(currentNode.val);

                // Add left child if it exists
                if (currentNode.left != null) {
                    queue.add(currentNode.left);
                }

                // Add right child if it exists
                if (currentNode.right != null) {
                    queue.add(currentNode.right);
                }
            }

            // Add current level list to result
            result.add(currentLevel);
        }

        return result;
    }
}

//1.Right view

class BeingZero{
    public List<Integer> rightViewOfTree(TreeNode r){
        List<Integer> ans = new ArrayList<>();
        if(r==null) return ans;
        Queue<TreeNode> q = new LinkedList<>();
        q.add(r);
        while(!q.isEmpty()){
            int size = q.size();
            for(int i=0;i<size;i++){
                TreeNode cur = q.remove();
                if(i== size-1) ans.add(cur.data);
                if(cur.left!=null) q.add(cur.left);
                if(cur.right!=null) q.add(cur.right);
            }
        }
        return ans;
    }
}

//2.Left view

class BeingZero {
    public List<Integer> leftViewOfTree(TreeNode r) {
        List<Integer> ans = new ArrayList<>();
        if (r == null) return ans;
        Queue<TreeNode> q = new LinkedList<>();
        q.add(r);
        while (!q.isEmpty()) {
            int len = q.size();
            for (int i = 0; i < len; i++) {
                TreeNode curr = q.remove();
                // Add the first node of each level to the answer
                if (i == 0) ans.add(curr.data);
                if (curr.left != null) q.add(curr.left);
                if (curr.right != null) q.add(curr.right);
            }
        }
        return ans;
    }
}

//3. ZigZag Traversal:

class BeingZero {
    public List<Integer> getZigZagLevel(TreeNode root) {
        List<Integer> ans1 = new ArrayList<>();
        if (root == null) return ans1;
        List<List<Integer>> ans = new ArrayList<>();
        Queue<TreeNode> q = new LinkedList<>();
        q.add(root);
        while (!q.isEmpty()) {
            List<Integer> inner = new ArrayList<>();
            int len = q.size();
            for (int i = 0; i < len; i++) {
                TreeNode curr = q.remove();
                inner.add(curr.data);
                if (curr.left != null) q.add(curr.left);
                if (curr.right != null) q.add(curr.right);
            }
            // Reverse every alternate level (0-based indexing)
            if (ans.size() % 2 == 0)
                Collections.sort(inner, Collections.reverseOrder());
            ans.add(inner);
        }
        // Flatten the 2D list into a single list
        for (List<Integer> l : ans) {
            for (int ele : l)
                ans1.add(ele);
        }
        return ans1;
    }
}


//4. No of Siblings and Cousins:

class BeingZero {
    // Count number of siblings of node x
    int countSiblings(TreeNode root, int x) {
        if (root == null || root.val == x) return 0;
        Queue<TreeNode> q = new LinkedList<>();
        q.add(root);
        while (!q.isEmpty()) {
            TreeNode curr = q.remove();
            if (curr.left != null && curr.right != null) {
                if (curr.left.val == x || curr.right.val == x)
                    return 1;
            }
            if (curr.left != null) q.add(curr.left);
            if (curr.right != null) q.add(curr.right);
        }
        return 0;
    }
    // Count number of cousins of node x
    int countCousins(TreeNode root, int x) {
        if (root == null || root.val == x) return 0;
        Queue<TreeNode> q = new LinkedList<>();
        q.add(root);
        boolean found = false;
        while (!q.isEmpty()) {
            int size = q.size();
            int cnt = 0;
            for (int i = 0; i < size; i++) {
                TreeNode curr = q.remove();
                // If curr is parent of x, do not add its children
                if ((curr.left != null && curr.left.val == x) ||
                    (curr.right != null && curr.right.val == x)) {
                    found = true;
                } else {
                    if (curr.left != null) {
                        q.add(curr.left);
                        cnt++;
                    }
                    if (curr.right != null) {
                        q.add(curr.right);
                        cnt++;
                    }
                }
            }
            if (found) return cnt;
        }
        return 0;
    }
}


//5.Nodes at k level:

class BeingZero {
    List<TreeNode> l;
    int solve(TreeNode r, int s, int k) {
        int ans = 0;
        l = new ArrayList<>();
        fph(r, s);
        ans += nodes(l.get(0), k--);
        for (int i = 1; i < l.size(); i++) {
            if (k == 0) {
                ans++;
                break;
            }
            TreeNode curr = l.get(i);
            if (curr.left == l.get(i - 1)) {
                ans += nodes(curr.right, k - 1);
            } else {
                ans += nodes(curr.left, k - 1);
            }
            k--;
        }
        return ans;
    }
    public void fph(TreeNode r, int s) {
        if (r == null) return;
        if (r.val == s) {
            l.add(r);
            return;
        }
        fph(r.left, s);
        if (l.size() != 0) {
            l.add(r);
            return;
        }
        fph(r.right, s);
        if (l.size() != 0) {
            l.add(r);
            return;
        }
        return;
    }
    public int nodes(TreeNode r, int k) {
        if (r == null) return 0;
        if (k == 0) return 1;
        Queue<TreeNode> q = new LinkedList<>();
        q.add(r);
        int lvl = 0;
        while (!q.isEmpty()) {
            int len = q.size();
            if (lvl == k) return len;
            while (len-- != 0) {
                TreeNode curr = q.remove();
                if (curr.left != null) q.add(curr.left);
                if (curr.right != null) q.add(curr.right);
            }
            lvl++;
        }
        return 0;
    }
}


//Vertical Order Traversal:

//1. Top view:

class Node {
    int key;
    Node left, right;
    Node(int data) {
        key = data;
        left = right = null;
    }
}
class Pair {
    Node node;
    int lvl;
    Pair(Node node, int lvl) {
        this.node = node;
        this.lvl = lvl;
    }
}
class BeingZero {

    List<Integer> top_view(Node root) {
        List<Integer> ans = new ArrayList<>();
        if (root == null) return ans;
        Queue<Pair> q = new LinkedList<>();
        q.add(new Pair(root, 0));
        Map<Integer, List<Integer>> map = new TreeMap<>();
        while (!q.isEmpty()) {
            int len = q.size();
            while (len-- != 0) {
                Pair p = q.remove();
                Node curr = p.node;
                int lvl = p.lvl;
                map.putIfAbsent(lvl, new ArrayList<>());
                map.get(lvl).add(curr.key);
                if (curr.left != null) q.add(new Pair(curr.left, lvl - 1));
                if (curr.right != null) q.add(new Pair(curr.right, lvl + 1));
            }
        }
        for (int k : map.keySet()) {
            ans.add(map.get(k).get(0)); // top view element
        }
        return ans;
    }
}

//2. Bottom view:

class BeingZero {
    List<Integer> bottom_view(Node root) {
        List<Integer> ans = new ArrayList<>();
        if (root == null) return ans;
        Queue<Pair> q = new LinkedList<>();
        q.add(new Pair(root, 0));
        Map<Integer, List<Integer>> map = new TreeMap<>();
        while (!q.isEmpty()) {
            int len = q.size();
            while (len-- != 0) {
                Pair p = q.remove();
                Node curr = p.node;
                int lvl = p.lvl;
                map.putIfAbsent(lvl, new ArrayList<>());
                map.get(lvl).add(curr.key);
                if (curr.left != null) q.add(new Pair(curr.left, lvl - 1));
                if (curr.right != null) q.add(new Pair(curr.right, lvl + 1));
            }
        }
        for (int k : map.keySet()) {
            List<Integer> col = map.get(k);
            ans.add(col.get(col.size() - 1)); // bottom view element
        }
        return ans;
    }
}

//3.LCA of BST:
class BeingZero {
    List<TreeNode> l1, l2;
    TreeNode lcaBST(TreeNode r, int p, int q) {
        l1 = new ArrayList<>();
        l2 = new ArrayList<>();
        fph(r, p, l1);
        fph(r, q, l2);
        int i = l1.size() - 1;
        int j = l2.size() - 1;

        TreeNode ans = null;
        while (i >= 0 && j >= 0 && l1.get(i) == l2.get(j)) {
            ans = l1.get(i);
            i--;
            j--;
        }
        return ans;
    }
    public void fph(TreeNode r, int s, List<TreeNode> l) {
        if (r == null) return;
        if (r.val == s) {
            l.add(r);
            return;
        }
        fph(r.left, s, l);
        if (l.size() != 0) {
            l.add(r);
            return;
        }
        fph(r.right, s, l);
        if (l.size() != 0) {
            l.add(r);
            return;
        }
    }
}

//Selializer & deserializer
//Binary lifting
//coverd & uncovered nodes
//morris traversal
//fph-- burn tree,nodes atk distance




//BIT MANIPULATION:


//1. Find Missing and Repeating Number

class FindMissingRepeated {

    // Function to find one repeated number and one missing number
    public List<Integer> solve(int[] arr, int n) {
        List<Integer> result = new ArrayList<>();
        int xorAll = 0;
        // Step 1: XOR all array elements
        for (int num : arr) {
            xorAll ^= num;
        }
        // Step 2: XOR numbers from 1 to n
        for (int i = 1; i <= n; i++) {
            xorAll ^= i;
        }
        // xorAll = repeated ^ missing
        // Step 3: Find rightmost set bit in xorAll
        int differingBit = -1;
        for (int bitPos = 0; bitPos < 32; bitPos++) {
            if (isBitSet(xorAll, bitPos)) {
                differingBit = bitPos;
                break;
            }
        }
        // Step 4: Divide numbers into two groups and XOR separately
        int xorGroup1 = 0;
        int xorGroup2 = 0;
        for (int num : arr) {
            if (isBitSet(num, differingBit)) xorGroup1 ^= num;
            else xorGroup2 ^= num;
        }
        for (int i = 1; i <= n; i++) {
            if (isBitSet(i, differingBit)) xorGroup1 ^= i;
            else xorGroup2 ^= i;
        }
        // Step 5: Determine which is repeated and which is missing
        int repeated = 0, missing = 0;
        for (int num : arr) {
            if (num == xorGroup1) {
                repeated = xorGroup1;
                missing = xorGroup2;
                break;
            } else if (num == xorGroup2) {
                repeated = xorGroup2;
                missing = xorGroup1;
                break;
            }
        }
        result.add(repeated);
        result.add(missing);
        return result;
    }
    // Helper function to check if a specific bit is set
    public static boolean isBitSet(int number, int bitPosition) {
        return (number & (1 << bitPosition)) != 0;
    }
}

//2. Finding Akela
import java.util.*;
import java.io.*;

class FindAkela {

    // This function finds the unique T-shirt number (AKELA)
    public long Solve(int numberOfPeople, int[] tshirtNumbers) {

        // This variable will store the XOR result
        long uniqueTshirtNumber = 0;

        // Loop through all T-shirt numbers
        for (int index = 0; index < numberOfPeople; index++) {

            // XOR current number with the result
            // Duplicate numbers cancel each other out
            uniqueTshirtNumber ^= tshirtNumbers[index];
        }

        // The remaining value is AKELA's T-shirt number
        return uniqueTshirtNumber;
    }
}


//3. Check, set, clear and flip bits
class Bit {
    // Clears the k-th bit of number (sets it to 0)
    public static int clearBit(int number, int bitPosition) {
        return number & ~(1 << bitPosition);
    }
    // Returns true if the k-th bit of number is set (1), false otherwise
    public static boolean isBitSet(int number, int bitPosition) {
        return (number & (1 << bitPosition)) != 0;
    }

}


//4. Triple trouble and similar problems
class TripleTrouble {
    /**
     * Computes a value based on bit counts across all numbers in the array.
     * For each bit position (0 to 63), if the count of numbers having that bit set
     * is NOT divisible by 3, that bit is added to the answer.
     */
    public long solve(long[] numbers) {
        long result = 0;
        // Iterate over all 64 possible bit positions for a long
        for (int bitPosition = 0; bitPosition < 64; bitPosition++) {
            int setBitCount = 0;
            // Count how many numbers have this bit set
            for (long value : numbers) {
                if (isBitSet(value, bitPosition)) {
                    setBitCount++;
                }
            }
            // If count is not divisible by 3, include this bit in the result
            if (setBitCount % 3 != 0) {
                result += (1L << bitPosition);
            }
        }
        return result;
    }
    //Checks whether the bit at a given position is set in the number.
    public static boolean isBitSet(long number, int bitPosition) {
        return ((1L << bitPosition) & number) != 0;
    }
}


//5. Power 2/4/8/16...
class Power{
    public boolean solve2(int num){
        if(num > 0 && ((num & num - 1) == 0)){
            return true;
        }
        return false;
    }
    public boolean solve4(int num) {
        if (num > 0 && ((num & (num - 1)) == 0) && (num % 3 == 1)) {
            return true;
        }
        return false;
    }
    public boolean solve8(int num) {
        if (num > 0 && ((num & (num - 1)) == 0) && (num % 7 == 1)) {
            return true;
        }
        return false;
    }
    public boolean solve16(int num) {
        if (num > 0 && ((num & (num - 1)) == 0) && (num % 15 == 1)) {
            return true;
        }
        return false;
    }
}


//6. Generate all subsets of a set
class GenerateAllSubsetsBitMal{
    public List<List<Integer>> solve(int[] inputArray) {
        List<List<Integer>> allSubsets = new ArrayList<>();
        int arrayLength = inputArray.length;

        // Sort input to keep elements in subsets ordered
        Arrays.sort(inputArray);

        int totalMasks = 1 << arrayLength;

        // Start from 1 to exclude empty subset
        for (int mask = 1; mask < totalMasks; mask++) {
            List<Integer> currentSubset = new ArrayList<>();

            for (int bitPosition = 0; bitPosition < arrayLength; bitPosition++) {
                if ((mask & (1 << bitPosition)) != 0) {
                    currentSubset.add(inputArray[bitPosition]);
                }
            }
            allSubsets.add(currentSubset);
        }

        // Sort subsets lexicographically
        Collections.sort(allSubsets, (subsetA, subsetB) -> {
            int minSize = Math.min(subsetA.size(), subsetB.size());

            for (int index = 0; index < minSize; index++) {
                if (!subsetA.get(index).equals(subsetB.get(index))) {
                    return subsetA.get(index) - subsetB.get(index);
                }
            }
            return subsetA.size() - subsetB.size();
        });

        return allSubsets;
    }
}


//Divide and Conquer:

//1. Binary Exponentiation
//2. Matrix Exponentiation
