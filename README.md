import random
import time

# Accept min and max temperature
min_temp = float(input("Enter minimum temperature: "))
max_temp = float(input("Enter maximum temperature: "))

if min_temp >= max_temp:
    print("Minimum should be less than maximum.")
else:
    while True:
        # Generate random temperature every 2 seconds
        temp = random.uniform(0, 100)
        print("Current Temperature:", round(temp, 2))

        # Compare with limits
        if temp < min_temp:
            print("Temperature is below minimum limit")
        elif temp > max_temp:
            print("Temperature is above maximum limit")
        else:
            print("Temperature is within limits")

        time.sleep(2)
