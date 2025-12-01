# 1)question

class Calculator:
    def __init__(self, a, b, operation):
        self.a = float(a)
        self.b = float(b)
        self.operation = operation.lower()

    def calculate(self):
        if self.operation == "add" or self.operation == "+":
            return self.a + self.b

        elif self.operation == "sub" or self.operation == "-":
            return self.a - self.b

        elif self.operation == "mul" or self.operation == "*":
            return self.a * self.b

        elif self.operation == "div" or self.operation == "/":
            if self.b == 0:
                return "Error: Division by zero!"
            return self.a / self.b

        else:
            return "Invalid operation"


# ---------- Example Usage ----------
a = 10
b = 5

calc = Calculator(a, b, "div")
result = calc.calculate()

print("Result:", result)
