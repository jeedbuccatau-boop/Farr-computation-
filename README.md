
print()
print("---------- CALCULATE FARE ----------")
print("[1] Regular Passenger")
print("[2] Student / Senior / PWD")

passenger = input("Passenger type: ")
distance = float(input("Enter distance in km: "))

if distance <= 0:
    print("Invalid distance.")

elif passenger == "1" or passenger == "2":
    fare = 35 + (max(0, distance - 1) * 5)

    if passenger == "2":
        fare = fare * 0.80

    print()
    print("----------- FARE RECEIPT -----------")
    print("Distance:", distance, "km")
    print("Total fare: PHP", round(fare, 2))

else:
    print("Invalid passenger type.")
    
