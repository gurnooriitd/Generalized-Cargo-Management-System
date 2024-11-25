
# Generalized Cargo Management System (GCMS)

### Overview
The **Generalized Cargo Management System (GCMS)** efficiently manages cargo bin assignments in a dynamic shipping environment. Cargo is categorized by color, each corresponding to specific bin assignment algorithms. The system optimizes space allocation while managing constraints like bin capacity and object sizes.

### Features:
- Unique IDs for bins and objects  
- Color-specific cargo handling using Compact Fit and Largest Fit algorithms  
- Support for dynamic addition, deletion, and querying of bins and objects  

---

### Files:
1. **gcms.py**  
   Implements the core `GCMS` class, managing bins and objects. Key functions include:  
   - `add_bin(bin_id, capacity)`  
   - `add_object(object_id, size, color)`  
   - `delete_object(object_id)`  
   - `object_info(object_id)`  
   - `bin_info(bin_id)`  

2. **bin.py**  
   Defines the `Bin` class, representing cargo bins with attributes like capacity and assigned objects.  

3. **object.py**  
   Defines the `Object` class, representing cargo objects with attributes like size, color, and placement information.  

4. **avl.py**  
   Contains the implementation of an AVL tree to manage and organize bins efficiently, ensuring operations maintain logarithmic complexity.  

5. **node.py**  
   Defines nodes used in the AVL tree structure.  

6. **exceptions.py**  
   Handles custom exceptions such as `NoBinFoundException`.  

7. **main.py**  
   Provides test cases and examples for debugging and validating the functionality of the system.  

---

### Cargo Handling Algorithms:
- **Compact Fit Algorithm (CFA)**  
  Places objects in the bin with the smallest available capacity that can accommodate the object.  
  Used for:  
  - Blue Cargo (chooses bin with least ID)  
  - Yellow Cargo (chooses bin with greatest ID)  

- **Largest Fit Algorithm (LFA)**  
  Places objects in the bin with the largest available capacity.  
  Used for:  
  - Red Cargo (chooses bin with least ID)  
  - Green Cargo (chooses bin with greatest ID)  

---

### Constraints:
- No use of Python dictionaries or sets.  
- Space complexity: O(n + m), where n is the number of bins and m is the number of objects.  
- Time complexity:  
  - `add_bin`, `add_object`, `delete_object`, `object_info`: O(log(n) + log(m))  
  - `bin_info`: O(log(n) + S), where S is the number of objects in the bin.  

---

This project demonstrates efficient space management and algorithmic problem-solving in a constrained environment, relevant for both educational and real-world applications.
