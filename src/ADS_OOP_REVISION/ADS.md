

### **Part B: "Undo System for Text Editor"**

A simple text editor uses a **stack** to support **undo** operations. Every time the user types a word, it is pushed onto the `actionStack`. The editor also supports a **"redo"** feature, but only **immediately after an undo**, and only **once**.

You are to design a system using **two stacks**:
- `actionStack`: stores words typed (most recent on top)
- `redoStack`: stores words that were undone (only one level of redo allowed)

Implement a method:
```java
public String undoLastAction()
```
- Pops the last word from `actionStack`
- Pushes it to `redoStack` (only if `redoStack` is empty — no multiple redos)
- Returns the undone word

Also implement:
```java
public String redoLastUndo()
```
- Only works if `redoStack` is not empty
- Moves the word back to `actionStack`
- Returns the word, or `null` if redo not possible


```java
import java.util.Stack;

public class TextEditor {
    private Stack<String> actionStack;
    private Stack<String> redoStack;

    public TextEditor() {
        actionStack = new Stack<>();
        redoStack = new Stack<>();
    }

    /**
     * Undo the last action: pop from actionStack, push to redoStack (if empty)
     * @return the undone word, or null if no action to undo
     */
    public String undoLastAction() {
        
    }

    /**
     * Redo the last undone action
     * @return the word restored, or null if redo not possible
     */
    public String redoLastUndo() {
        
    }
}
```

---

**[7 marks]**

> 🎯 *Tests understanding of stack use in real systems and constraints.*

---

## **Question 3: Binary Trees – Diagram-Based Operations**

### **Given**:
A **binary search tree (BST)** with the following nodes inserted in this order:  
**50, 30, 70, 20, 40, 60, 80**

---

### **Part A**:
Draw the **final structure** of the BST after all insertions. Label all nodes.

**[3 marks]**

---

### **Part B**:
Now perform the following operations **in sequence**, drawing the tree **after each step**:

1. Insert **35**
2. Insert **75**
3. Delete **30** (use standard BST deletion: if two children, replace with **in-order predecessor**)
4. Delete **70**

Show the tree after **each** operation.

**[8 marks – 2 each]**

> 📌 *Ensure diagrams are clear, with left/right children correctly positioned.*

---

### **Part C**:
After the final tree, state:
- The **height** of the tree
- Whether it is **balanced**
- One advantage of a **balanced BST** over an unbalanced one

**[3 marks]**

---

## **Question 4: Vocabulary & Diagram Quiz**

### **Part A: Definitions**
Define the following terms (1 mark each):

1. Node
2. Singly linked list
3. Stack (LIFO)
4. Binary search tree (BST)
5. Balanced tree
6. In-order traversal
7. Overflow (in stack context)
8. Head (in linked list)

**[8 marks]**

---

### **Part B: Diagram Interpretation**

You are given the following **singly linked list diagram**:

```
[Anna] -> [Bob] -> [Cara] -> null
```

Each node contains a `Customer` object.

1. Label the **head node**.
2. What is the **successor** of Bob?
3. What happens if the reference from Bob to Cara is lost?
4. Why can't you traverse from Cara to Bob?

**[4 marks]**

---

### **Part C: Tree Type Identification**

Given three tree diagrams (describe them verbally or sketch in exam):

- **Tree A**: All leaves at same level, full at every level
- **Tree B**: Skewed heavily to the left, height = n-1
- **Tree C**: Height difference between left and right subtrees ≤ 1 at every node

Identify each as:
- Full binary tree
- Skewed (unbalanced) tree
- Balanced BST

And state which would give **best search performance** and why.

**[5 marks]**

---