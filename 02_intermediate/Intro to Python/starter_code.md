# Planetary WeightsDownload Project

```bash
MARS_MULTIPLE = 0.378

def mars_weight():

  earth_weight = float(input('Enter a weight on Earth: '))
  mars_weight = round(earth_weight * MARS_MULTIPLE, 2)
  print(f'The equivalent weight on Mars: {mars_weight}')


gravity_constants = {
  "Mercury": 0.376,
  "Venus": 0.889,
  "Mars": 0.378,
  "Jupiter": 2.36,
  "Saturn": 1.081,
  "Uranus": 0.815,
  "Neptune": 1.14,
}

def planetary_weight():
  earth_weight = float(input("Enter a weight on Earth: "))
  planet = input("Enter a planet: ")

  if (planet in gravity_constants):
    weight_on_planet = round(earth_weight * gravity_constants[planet], 2)
    print(f"The equivalent weight on {planet}: {weight_on_planet} kg")
  else:
    print("Invalid planet name! Please enter a valid planet.")

def main():
    choice = input("Do you want to calculate weight for Mars only or other planets? (Mars/Planet): ").strip().lower()
    if choice == "mars":
        mars_weight()
    elif choice == "planet":
        planetary_weight()
    else:
        print("Invalid choice! Please enter 'Mars' or 'Planet'.")

if __name__ == "__main__":
    main()



```
