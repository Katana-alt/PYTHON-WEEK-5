# PYTHON-WEEK-5
# Base class
class Smartphone:
    def __init__(self, brand, model, storage):
        self.brand = brand
        self.model = model
        self.storage = storage

    def display_info(self):
        print(f"{self.brand} {self.model} with {self.storage}GB storage")

    def call(self, number):
        print(f"Calling {number} from {self.model}...")

# Derived class with inheritance
class SmartphoneWithCamera(Smartphone):
    def __init__(self, brand, model, storage, camera_megapixels):
        super().__init__(brand, model, storage)  # Call the parent constructor
        self.camera_megapixels = camera_megapixels

    def take_photo(self):
        print(f"Taking a photo with a {self.camera_megapixels}MP camera")

# Example usage
phone1 = Smartphone("BrandX", "ModelY", 64)
phone1.display_info()
phone1.call("123-456-7890")

camera_phone = SmartphoneWithCamera("BrandZ", "ModelA", 128, 48)
camera_phone.display_info()
camera_phone.take_photo()
