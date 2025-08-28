# Matplotlib Basics

## 1. What is Matplotlib?
Matplotlib is a Python library used to create static, animated, and interactive plots.  
It’s widely used for data visualization in Python.  
It is especially useful with libraries like **NumPy** and **pandas**.  

---

## 2. How do you install Matplotlib?
Use pip:

```bash
pip install matplotlib
```

----------

### **3. What is the use of `pyplot` in Matplotlib?**

-   `pyplot` is a submodule of Matplotlib.
    
-   It provides a MATLAB-like interface for making plots easily.
    
-   Commonly imported as:
```bash
import matplotlib.pyplot as plt    
```
----------

### **4. How do you create a basic line plot?**

-   Example:
```bash  
import matplotlib.pyplot as plt
x = [1, 2, 3]
y = [4, 5, 6]
plt.plot(x, y)
plt.show()
```

----------

### **5. How can you add labels and a title to a plot?**

-   Use these functions:
```bash
plt.xlabel('X-axis label')
plt.ylabel('Y-axis label')
plt.title('Title of the Plot')
```
    
----------

### **6. How do you display multiple plots on the same graph?**

-   Plot multiple lines by calling `plt.plot()` multiple times before `plt.show()`:
```bash 
plt.plot(x1, y1)
plt.plot(x2, y2)
```
    
----------

### **7. What is the purpose of `plt.legend()`?**

-   It shows labels for different plotted lines.
    
-   Use `label` in `plot()` and call `plt.legend()`:

```bash     
plt.plot(x, y, label='Line A')
plt.legend()
```
----------

### **8. How do you create subplots?**

-   Use `plt.subplot(rows, cols, plot_number)`:

```bash   
plt.subplot(1, 2, 1)
plt.plot(x1, y1)
    
plt.subplot(1, 2, 2)
plt.plot(x2, y2)
```   

----------

### **9. What is the difference between `plt.plot()` and `plt.scatter()`?**

-   `plt.plot()` connects points with lines (line plot).
    
-   `plt.scatter()` plots individual points (scatter plot).
    
----------

### **10. How can you customize line styles and colors?**

-   Use parameters like `color`, `linestyle`, `linewidth`:

```bash 
plt.plot(x, y, color='red', linestyle='--', linewidth=2)
```
    
----------

### **11. How do you save a plot as an image?**

-   Use `plt.savefig()`:
    
```bash
plt.savefig('myplot.png')
```
    
----------

### **12. How do you change figure size?**

-   Use `plt.figure()` with `figsize`:
    
```bash
plt.figure(figsize=(10, 5))
```
    
----------

### **13. What is a histogram and how do you create it in Matplotlib?**

-   A histogram shows the distribution of a dataset.
    
-   Use `plt.hist()`:
    
```bash
plt.hist(data, bins=10)
```
----------

### **14. How can you plot a bar chart?**

-   Use `plt.bar()`:
    
```bash 
plt.bar(categories, values)
```

----------

### **15. How do you rotate x-axis labels for better visibility?**

-   Use `plt.xticks(rotation=angle)`:
    
```bash 
plt.xticks(rotation=45)
```   

----------
