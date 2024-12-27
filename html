// project structure
/src
  /main
    /java
      /com/example/webapp
        /controller
          - HomeController.java
          - UserController.java
          - ProductController.java
          - OrderController.java
        /service
          - UserService.java
          - ProductService.java
          - OrderService.java
        /model
          - User.java
          - Product.java
          - Order.java
          - Review.java
        /repository
          - UserRepository.java
          - ProductRepository.java
          - OrderRepository.java
        - WebAppApplication.java
    /resources
      /static
        /css
          - style.css
        /js
          - app.js
      /templates
        - home.html
        - about.html
        - contact.html
        - userProfile.html
        - productList.html
        - productDetails.html
        - login.html
        - orderSummary.html
    /application.properties

//web app application
package com.example.webapp;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
import org.springframework.boot.web.servlet.ServletComponentScan;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.config.annotation.web.configuration.WebSecurityConfigurerAdapter;

@SpringBootApplication
public class WebAppApplication {

    public static void main(String[] args) {
        SpringApplication.run(WebAppApplication.class, args);
    }
}

@EnableWebSecurity
class SecurityConfig extends WebSecurityConfigurerAdapter {
    @Override
    protected void configure(HttpSecurity http) throws Exception {
        http
            .authorizeRequests()
                .antMatchers("/", "/about", "/contact", "/login", "/register").permitAll()
                .antMatchers("/admin/").hasRole("ADMIN")
                .anyRequest().authenticated()
            .and()
            .formLogin()
                .loginPage("/login")
                .permitAll()
            .and()
            .logout()
                .permitAll();
    }
}


//user controller
package com.example.webapp.controller;

import com.example.webapp.model.User;
import com.example.webapp.service.UserService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;

@Controller
public class UserController {

    @Autowired
    private UserService userService;

    @GetMapping("/login")
    public String login() {
        return "login";
    }

    @PostMapping("/login")
    public String authenticateUser(User user, Model model) {
        boolean isValidUser = userService.authenticateUser(user);
        if (isValidUser) {
            model.addAttribute("user", user);
            return "userProfile";
        } else {
            model.addAttribute("message", "Invalid credentials");
            return "login";
        }
    }

    @GetMapping("/register")
    public String register() {
        return "register";
    }

    @PostMapping("/register")
    public String registerUser(User user, Model model) {
        userService.saveUser(user);
        model.addAttribute("message", "User registered successfully!");
        return "login";
    }
}


//product controller
package com.example.webapp.controller;

import com.example.webapp.model.Product;
import com.example.webapp.service.ProductService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;

@Controller
public class ProductController {

    @Autowired
    private ProductService productService;

    @GetMapping("/products")
    public String viewProducts(Model model) {
        model.addAttribute("products", productService.getAllProducts());
        return "productList";
    }

    @GetMapping("/product/{id}")
    public String viewProductDetails(@PathVariable("id") int id, Model model) {
        model.addAttribute("product", productService.getProductById(id));
        return "productDetails";
    }
}


//order controller
package com.example.webapp.controller;

import com.example.webapp.model.Order;
import com.example.webapp.service.OrderService;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;

@Controller
public class OrderController {

    @Autowired
    private OrderService orderService;

    @GetMapping("/orderSummary")
    public String viewOrderSummary(Model model) {
        model.addAttribute("orders", orderService.getAllOrders());
        return "orderSummary";
    }
}


//product service
package com.example.webapp.service;

import com.example.webapp.model.Product;
import org.springframework.stereotype.Service;

@Service
public class ProductService {

    public Product[] getAllProducts() {
        return new Product[] {
            new Product(1, "Car Model A", 1000),
            new Product(2, "Car Model B", 1200),
            new Product(3, "Car Model C", 1500)
        };
    }

    public Product getProductById(int id) {
        // Simulating fetching product by id from a database
        return new Product(id, "Car Model " + id, 1000 + (id * 100));
    }
}


//order service
package com.example.webapp.service;

import com.example.webapp.model.Order;
import org.springframework.stereotype.Service;

@Service
public class OrderService {

    public Order[] getAllOrders() {
        return new Order[] {
            new Order(1, "Order A", 1000),
            new Order(2, "Order B", 1200),
            new Order(3, "Order C", 1500)
        };
    }
}


//user model
package com.example.webapp.model;

public class User {
    private String username;
    private String password;
    private String email;

    public User(String username, String password, String email) {
        this.username = username;
        this.password = password;
        this.email = email;
    }

    // Getters and Setters
    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }
}


//product model
package com.example.webapp.model;

public class Product {
    private int id;
    private String name;
    private double price;

    public Product(int id, String name, double price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }

    // Getters and Setters
    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getPrice() {
        return price;
    }

    public void setPrice(double price) {
        this.price = price;
    }
}


//order summary
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Order Summary</title>
    <link rel="stylesheet" href="/css/style.css">
</head>
<body>
    <header>
        <h1>Your Orders</h1>
    </header>
    <main>
        <h2>Order Details</h2>
        <table>
            <tr>
                <th>Order ID</th>
                <th>Name</th>
                <th>Price</th>
            </tr>
            <tr th:each="order : ${orders}">
                <td th:text="${order.id}"></td>
                <td th:text="${order.name}"></td>
                <td th:text="${order.price}"></td>
            </tr>
        </table>
    </main>
    <footer>
        <p>&copy; 2024 Car Racing WebApp</p>
    </footer>
</body>
</html>


//style css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 20px;
    text-align: center;
}

main {
    padding: 20px;
    text-align: center;
}

table {
    width: 80%;
    margin: 20px auto;
    border-collapse: collapse;
}

table th, table td {
    border: 1px solid #ddd;
    padding: 10px;
}

footer {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
}





// leet code 
// two sum
import java.util.HashMap;
public class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer, Integer> numMap = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            int complement = target - nums[i];
            if (numMap.containsKey(complement)) {
                return new int[] { numMap.get(complement), i };
            }
            numMap.put(nums[i], i);
        }
        return new int[] {};
    }
}


//Add Two Numbers
public class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode dummy = new ListNode(0);
        ListNode current = dummy;
        int carry = 0;
        while (l1 != null || l2 != null || carry != 0) {
            int sum = carry;
            if (l1 != null) {
                sum += l1.val;
                l1 = l1.next;
            }
            if (l2 != null) {
                sum += l2.val;
                l2 = l2.next;
            }
            carry = sum / 10;
            current.next = new ListNode(sum % 10);
            current = current.next; 
        }

        return dummy.next;
    }
}

//Longest Substring Without Repeating Characters
import java.util.HashSet;

public class Solution {
    
    public static int lengthOfLongestSubstring(String s) {
        // HashSet to store unique characters in the current window
        HashSet<Character> charSet = new HashSet<>();
        int left = 0;  // Left pointer of the sliding window
        int maxLen = 0;  // Maximum length of the substring without repeating characters
        
        // Iterate through the string with the right pointer
        for (int right = 0; right < s.length(); right++) {
            // If the character is already in the set, move the left pointer
            while (charSet.contains(s.charAt(right))) {
                charSet.remove(s.charAt(left));
                left++;
            }
            
            // Add the current character to the set
            charSet.add(s.charAt(right));

            // Update the maximum length of the substring
            maxLen = Math.max(maxLen, right - left + 1);
        }

        return maxLen;
    }

    public static void main(String[] args) {
        // Example 1: "abcabcbb"
        String s1 = "abcabcbb";
        System.out.println("Longest substring length: " + lengthOfLongestSubstring(s1));  // Output: 3

        // Example 2: "bbbbb"
        String s2 = "bbbbb";
        System.out.println("Longest substring length: " + lengthOfLongestSubstring(s2));  // Output: 1

        // Example 3: "pwwkew"
        String s3 = "pwwkew";
        System.out.println("Longest substring length: " + lengthOfLongestSubstring(s3));  // Output: 3
    }
}

//Median of Two Sorted Arrays
public class Solution {
    public double findMedianSortedArrays(int[] nums1, int[] nums2) {
        // Ensure nums1 is the smaller array for binary search efficiency
        if (nums1.length > nums2.length) {
            int[] temp = nums1;
            nums1 = nums2;
            nums2 = temp;
        }

        int m = nums1.length;
        int n = nums2.length;
        
        int left = 0, right = m;

        while (left <= right) {
            // Partition nums1
            int partition1 = (left + right) / 2;
            // Partition nums2, derived from partition1
            int partition2 = (m + n + 1) / 2 - partition1;

            // Find the elements around the partition in nums1 and nums2
            int maxLeft1 = (partition1 == 0) ? Integer.MIN_VALUE : nums1[partition1 - 1];
            int minRight1 = (partition1 == m) ? Integer.MAX_VALUE : nums1[partition1];

            int maxLeft2 = (partition2 == 0) ? Integer.MIN_VALUE : nums2[partition2 - 1];
            int minRight2 = (partition2 == n) ? Integer.MAX_VALUE : nums2[partition2];

            // Check if we have found the correct partition
            if (maxLeft1 <= minRight2 && maxLeft2 <= minRight1) {
                // If the combined length is odd, return the maximum of the left partition
                if ((m + n) % 2 == 1) {
                    return Math.max(maxLeft1, maxLeft2);
                } else {
                    // If the combined length is even, return the average of the middle two elements
                    return (Math.max(maxLeft1, maxLeft2) + Math.min(minRight1, minRight2)) / 2.0;
                }
            } else if (maxLeft1 > minRight2) {
                // Move partition1 to the left
                right = partition1 - 1;
            } else {
                // Move partition1 to the right
                left = partition1 + 1;
            }
        }

        throw new IllegalArgumentException("Input arrays are not sorted");
    }
}


//Longest Palindromic Substring
public class Solution {
    public String longestPalindrome(String s) {
        if (s == null || s.length() == 0) {
            return "";
        }

        String longest = "";
        
        for (int i = 0; i < s.length(); i++) {
            // Check for palindrome with a single character center
            String oddPalindrome = expandAroundCenter(s, i, i);
            // Check for palindrome with two character center
            String evenPalindrome = expandAroundCenter(s, i, i + 1);
            
            // Update the longest palindrome if necessary
            if (oddPalindrome.length() > longest.length()) {
                longest = oddPalindrome;
            }
            if (evenPalindrome.length() > longest.length()) {
                longest = evenPalindrome;
            }
        }
        
        return longest;
    }
    
    // Helper function to expand around the center
    private String expandAroundCenter(String s, int left, int right) {
        while (left >= 0 && right < s.length() && s.charAt(left) == s.charAt(right)) {
            left--;
            right++;
        }
        // Return the palindrome substring
        return s.substring(left + 1, right);
    }
}


//Zigzag Conversion
public class Solution {
    public String convert(String s, int numRows) {
        // Edge case: if the number of rows is 1, no zigzag is possible
        if (numRows == 1) {
            return s;
        }
        
        // Initialize an array of StringBuilder to store each row
        StringBuilder[] rows = new StringBuilder[numRows];
        for (int i = 0; i < numRows; i++) {
            rows[i] = new StringBuilder();
        }
        
        int currentRow = 0;
        boolean goingDown = false;
        
        // Iterate through the string and fill the rows
        for (char c : s.toCharArray()) {
            rows[currentRow].append(c);
            
            // If we're at the top or bottom row, change the direction
            if (currentRow == 0 || currentRow == numRows - 1) {
                goingDown = !goingDown;
            }
            
            // Move to the next row
            currentRow += goingDown ? 1 : -1;
        }
        
        // Combine all rows into one string
        StringBuilder result = new StringBuilder();
        for (StringBuilder row : rows) {
            result.append(row);
        }
        
        return result.toString();
    }
}


//Reverse Integer
public class Solution {
    public int reverse(int x) {
        int result = 0;
        int max = Integer.MAX_VALUE / 10;
        int min = Integer.MIN_VALUE / 10;
        
        while (x != 0) {
            int digit = x % 10; // Get the last digit
            x /= 10; // Remove the last digit from x
            
            // Check for overflow before updating result
            if (result > max || (result == max && digit > 7)) {
                return 0; // Overflow for positive numbers
            }
            if (result < min || (result == min && digit < -8)) {
                return 0; // Overflow for negative numbers
            }
            
            // Update result with the new digit
            result = result * 10 + digit;
        }
        
        return result;
    }
}


// String to Integer (atoi)
public class Solution {
    public int myAtoi(String s) {
        int i = 0;
        int n = s.length();
        
        // Step 1: Skip leading whitespaces
        while (i < n && s.charAt(i) == ' ') {
            i++;
        }

        // Step 2: Check for the sign
        int sign = 1;
        if (i < n && (s.charAt(i) == '+' || s.charAt(i) == '-')) {
            sign = (s.charAt(i) == '-') ? -1 : 1;
            i++;
        }

        // Step 3: Read the digits and convert them to an integer
        long result = 0;  // Use long to prevent overflow during calculation
        while (i < n && Character.isDigit(s.charAt(i))) {
            result = result * 10 + (s.charAt(i) - '0');
            i++;
            
            // Step 4: Check for overflow
            if (result > Integer.MAX_VALUE) {
                return sign == 1 ? Integer.MAX_VALUE : Integer.MIN_VALUE;
            }
        }

        // Step 5: Apply the sign and return the result
        return (int) (result * sign);
    }
}


//Palindrome Number
public class Solution {
    public boolean isPalindrome(int x) {
        // If the number is negative or if the number ends with 0 but is not 0 itself, return false
        if (x < 0 || (x % 10 == 0 && x != 0)) {
            return false;
        }
        
        int reversed = 0;
        while (x > reversed) {
            // Build the reversed half of the number
            reversed = reversed * 10 + x % 10;
            x /= 10;
        }
        
        // If the original number is equal to the reversed half or if it is the same when divided by 10 (for odd length numbers)
        return x == reversed || x == reversed / 10;
    }
}



//Regular Expression Matching
public class Solution {
    public boolean isMatch(String s, String p) {
        int m = s.length();
        int n = p.length();
        
        // dp[i][j] represents whether s[0..i-1] matches p[0..j-1]
        boolean[][] dp = new boolean[m + 1][n + 1];
        
        // Initial condition: empty string matches empty pattern
        dp[0][0] = true;
        
        // Handle the case when the pattern starts with a '*' (matching empty string)
        for (int j = 1; j <= n; j++) {
            if (p.charAt(j - 1) == '*') {
                dp[0][j] = dp[0][j - 2];  // '*' means zero occurrences of the previous character
            }
        }
        
        // Fill the dp table
        for (int i = 1; i <= m; i++) {
            for (int j = 1; j <= n; j++) {
                if (p.charAt(j - 1) == s.charAt(i - 1) || p.charAt(j - 1) == '.') {
                    // If characters match or pattern has '.', carry forward the previous result
                    dp[i][j] = dp[i - 1][j - 1];
                } else if (p.charAt(j - 1) == '*') {
                    // Case 1: '*' represents zero occurrences of the preceding character
                    dp[i][j] = dp[i][j - 2];
                    
                    // Case 2: '*' represents
