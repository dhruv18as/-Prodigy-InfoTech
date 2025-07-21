def convert_temperature(value, unit):
    unit = unit.lower()

    if unit == "celsius":
        fahrenheit = (value * 9 / 5) + 32
        kelvin = value + 273.15
        print(f"\nInput: {value}°C")
        print(f"Fahrenheit: {fahrenheit:.2f}°F")
        print(f"Kelvin: {kelvin:.2f}K")

    elif unit == "fahrenheit":
        celsius = (value - 32) * 5 / 9
        kelvin = celsius + 273.15
        print(f"\nInput: {value}°F")
        print(f"Celsius: {celsius:.2f}°C")
        print(f"Kelvin: {kelvin:.2f}K")

    elif unit == "kelvin":
        celsius = value - 273.15
        fahrenheit = (celsius * 9 / 5) + 32
        print(f"\nInput: {value}K")
        print(f"Celsius: {celsius:.2f}°C")
        print(f"Fahrenheit: {fahrenheit:.2f}°F")

    else:
        print("❌ Invalid unit. Please enter Celsius, Fahrenheit, or Kelvin.")

# Main program
print("🌡️ Temperature Converter (Celsius, Fahrenheit, Kelvin)")
try:
    value = float(input("Enter the temperature value: "))
    unit = input("Enter the unit (Celsius/Fahrenheit/Kelvin): ")
    convert_temperature(value, unit)
except ValueError:
    print("❌ Please enter a valid number for the temperature.")
