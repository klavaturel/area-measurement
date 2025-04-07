# area-measurement
import math

def calculate_area(shape, **kwargs):
    """Calculate the area of different geometric shapes."""
    if shape == "circle":
        radius = kwargs.get("radius", 0)
        return math.pi * radius ** 2
    
    elif shape == "rectangle":
        length = kwargs.get("length", 0)
        width = kwargs.get("width", 0)
        return length * width
    
    elif shape == "triangle":
        base = kwargs.get("base", 0)
        height = kwargs.get("height", 0)
        return 0.5 * base * height
    
    elif shape == "square":
        side = kwargs.get("side", 0)
        return side ** 2
    
    elif shape == "trapezoid":
        base1 = kwargs.get("base1", 0)
        base2 = kwargs.get("base2", 0)
        height = kwargs.get("height", 0)
        return 0.5 * (base1 + base2) * height
    
    else:
        return "Unknown shape"

# Example usage
def main():
    print("Circle area:", calculate_area("circle", radius=5))
    print("Rectangle area:", calculate_area("rectangle", length=10, width=5))
    print("Triangle area:", calculate_area("triangle", base=8, height=4))
    print("Square area:", calculate_area("square", side=6))
    print("Trapezoid area:", calculate_area("trapezoid", base1=6, base2=8, height=4))

if __name__ == "__main__":
    main()
