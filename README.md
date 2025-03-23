# Parent class
class Smartphone:
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.price = price

    def get_info(self):
        return f"{self.brand} {self.model} costs ${self.price}"

# Child class (Inheritance)
class SmartPhoneWithCamera(Smartphone):
    def __init__(self, brand, model, price, camera_megapixels):
        super().__init__(brand, model, price)
        self.camera_megapixels = camera_megapixels

    def take_photo(self):
        return f"Taking a photo with {self.camera_megapixels} MP camera!"

# Creating objects
phone1 = Smartphone("Samsung", "Galaxy S21", 799)
phone2 = SmartPhoneWithCamera("Apple", "iPhone 14", 999, 48)

# Testing the methods
print(phone1.get_info())  # Output: Samsung Galaxy S21 costs $799
print(phone2.get_info())  # Output: Apple iPhone 14 costs $999
print(phone2.take_photo())  # Output: Taking a photo with 48 MP camera!


# Parent class
class Vehicle:
    def move(self):
        pass  # Placeholder method (to be overridden)

# Child classes
class Car(Vehicle):
    def move(self):
        return "Driving 🚗"

class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"

class Boat(Vehicle):
    def move(self):
        return "Sailing ⛵"

# Testing polymorphism
vehicles = [Car(), Plane(), Boat()]
for vehicle in vehicles:
    print(vehicle.move())
    
    Driving 🚗
Flying ✈️
Sailing ⛵


![1000091753](https://github.com/user-attachments/assets/48ef301e-ca25-4240-9669-72ef6f0c2afb)

