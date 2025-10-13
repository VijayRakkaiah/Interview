# 🧠 PyTorch `nn.Module` Interview Questions

## 1. What is `nn.Module` in PyTorch?

**Answer:**  
Think of `nn.Module` like a LEGO blueprint. It tells PyTorch how to build and connect pieces (layers) of a neural network. Every model you make is built from this blueprint.
 
---

## 2. Why do we use `nn.Module`?

**Answer:**  
We use it so we don’t have to build everything from scratch. It makes building, saving, and reusing models much easier.

---

## 3. How do you create a custom model using `nn.Module`?

**Answer:**  
You create a class that uses `nn.Module` as its parent. Like this:

```python
import torch.nn as nn

class MyModel(nn.Module):
    def __init__(self):
        super().__init__()
        # Add layers here
        self.linear = nn.Linear(10, 5)

    def forward(self, x):
        # Tell how data flows through layers
        return self.linear(x)
```

---

## 4. What is the purpose of the `__init__()` method in `nn.Module`?

**Answer:**  
It’s where you **build the parts** of your model — like choosing what layers you’ll use (like LEGO bricks).

---

## 5. What does the `forward()` method do?

**Answer:**  
It shows **how data flows** through the layers you built — like giving directions to the LEGO pieces.

---

## 6. Why do we use `super().__init__()` in the constructor?

**Answer:**  
It tells PyTorch to **set up all the magic** behind the scenes, so your model can work properly.

---

## 7. What happens if you forget to call `super().__init__()`?

**Answer:**  
Your model might not work correctly. It’s like skipping the step where LEGO instructions say "check all your pieces first."

---

## 8. What is the difference between `nn.Module` and `nn.Sequential`?

**Answer:**  
- `nn.Module`: You can build **custom** and complex models.  
- `nn.Sequential`: You stack layers **in order**, one after another — good for simple models.

---

## 9. Can a `nn.Module` contain other `nn.Module`s?

**Answer:**  
Yes! Just like a LEGO set can have mini LEGO sets inside. You can build modules inside modules.

---

## 10. How do you get the list of all parameters in your model?

**Answer:**  
Use `model.parameters()`. It shows all the things your model is learning, like weights and biases.

---

## 11. What is `model.eval()` and why is it important?

**Answer:**  
It puts the model in **test mode**, so it doesn’t do things like dropout. It’s like telling your LEGO model “stop training, just perform now.”

---

## 12. What is `model.train()` used for?

**Answer:**  
It tells your model, “We’re training now!” — so it uses layers like dropout or batch norm properly.

---

## 13. How do you save a model created from `nn.Module`?

**Answer:**  
You save its brain (the weights):

```python
torch.save(model.state_dict(), 'model.pth')
```

---

## 14. How do you load a saved model?

**Answer:**

```python
model.load_state_dict(torch.load('model.pth'))
model.eval()
```

It’s like giving your model back its memory.

---

## 15. What’s the difference between `model()` and `model.forward()`?

**Answer:**  
Using `model()` is better — it calls `forward()` but also does **extra safety checks**. Like putting on a helmet before riding a bike.


---


