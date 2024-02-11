# Heathy-lifestyle-
#Calorie Counter: Write a program that asks the user for their 
#age, weight, and activity level, then calculates their daily 
#calorie goal based on recommended guidelines. Use if-
#else statements to adjust the goal based on the user's activity 
#level.
# Get user input
age = int(input("Enter your age: "))
weight = int(input("Enter your weight in kilograms: "))
activity_level = input("Enter your activity level (sedentary, moderate, active): ") 
# Constants for calorie calculation
sedentary_multiplier = 1.2
moderate_multiplier = 1.55
active_multiplier = 1.9
# Calorie calculation based on activity level
if activity_level.lower() == "sedentary":
    calorie_goal = int(30 * weight * sedentary_multiplier)
elif activity_level.lower() == "moderate":
    calorie_goal = int(30 * weight * moderate_multiplier)
elif activity_level.lower() == "active":
    calorie_goal = int(30 * weight * active_multiplier)
else:
    print("Invalid activity level. Please enter sedentary, moderate, or active.")
    exit()
# result
print(f"Your daily calorie goal is: {calorie_goal} calories")
#2.Sleep Tracker: Create a program that asks the user for their 
#bedtime and wake-up time, then calculates their total sleep 
#duration. Use if statements to determine if they met the recommended sleep amount and 
#provide feedback accordingly.
from datetime import datetime
# User input for bedtime and wake-up time
bedtime = input("Enter your bedtime (in HH:MM format): ")
wake_up_time = input("Enter your wake-up time (in HH:MM format): ")
# Convert bedtime and wake-up time strings to datetime objects
bedtime_dt = datetime.strptime(bedtime, "%H:%M")
wake_up_time_dt = datetime.strptime(wake_up_time, "%H:%M")
# Calculate sleep duration by subtracting bedtime from wake-up time
sleep_duration = wake_up_time_dt - bedtime_dt
# Calculate recommended sleep duration (in hours)
recommended_sleep_duration = 8
# recommended sleep amount
if sleep_duration >= recommended_sleep_duration:
    print("Great job! You met the recommended sleep amount.")
else:
    print("You should try to get more sleep. Aim for at least 8 hours.")
# Print the total sleep duration
print("Your total sleep duration was:", sleep_duration)
#3Hydration Helper: Design a program that prompts the user for their weight and desired level of 
#hydration (e.g., light, moderate, intense exercise). Use nested if-else statements to suggest the 
#amount of water they should drink throughout the day.
# Hydration Helper Program
# Get user input for weight and desired level of hydration
weight = int(input("Enter your weight in kilograms: "))
hydration_level = input("Enter your desired level of hydration (light, moderate, intense): ").lower()

# Define water intake recommendations based on hydration levels
light_hydration = 30  # milliliters per kilogram
moderate_hydration = 40  # milliliters per kilogram
intense_hydration = 50  # milliliters per kilogram

# Calculate recommended water intake based on weight and hydration level
if hydration_level == "light":
    recommended_water_intake = weight * light_hydration
elif hydration_level == "moderate":
    recommended_water_intake = weight * moderate_hydration
elif hydration_level == "intense":
    recommended_water_intake = weight * intense_hydration
else:
    print("Invalid hydration level. Please choose light, moderate, or intense.")
    recommended_water_intake = 0

# Provide feedback on recommended water intake
if recommended_water_intake > 0:
    print(f"To stay hydrated at a {hydration_level} level, aim to drink approximately {recommended_water_intake:.2f} milliliters of water throughout the day.")
    
