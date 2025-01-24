# Car Rental Management System

Welcome to the **Car Rental Management System** project! This C++ application allows customers to rent cars, calculate the rental fee based on the number of days rented, and generate a detailed invoice for the transaction. The project demonstrates the application of object-oriented programming (OOP) concepts.

---

## Features

- **Welcome Screen**: Greets the customer with a welcome message.
- **Car Selection**: Allows customers to choose from three available car models.
- **File Reader**: Displays the specifications of the selected car model.
- **User Data Input**: Captures customer details, selected car number, and rental duration.
- **Invoice Generation**: Calculates and displays the total rental fee in a detailed invoice format.
- **File Integration**: Reads external files to enhance interactivity and provide specific car details.

---

## Functions and Their Purpose

### 1. `welcome()`
- Displays the welcome message by reading content from `welcome.txt`.
- Provides a smooth user experience by simulating loading delays.

### 2. `fileReader(char carFile[20])`
- Reads and displays the content of a file passed as an argument (e.g., car specifications).
- Handles file errors gracefully if the file is not found.

### 3. `data()`
- Collects user details, such as:
  - Customer Name
  - Selected Car Model
  - Car Number
  - Number of Days for Rent
- Ensures the user selects a valid car model.

### 4. `invoiceAmount()`
- Calculates the rental fee based on the car model and the number of rental days.
  - **Toyota 2021**: $150/day
  - **Hyundai 2019**: $160/day
  - **Ford 2020**: $175/day

### 5. `invoiceRecord()`
- Generates and displays a detailed invoice with:
  - Customer Name
  - Selected Car Model
  - Car Number
  - Number of Rental Days
  - Total Rental Fee
  
- Reads and displays a thank-you message from `thanks.txt`.

### 6. `main()`
- Creates an object of the `Rent` class and calls the respective functions in sequence.

---

## Text Files Used

### `welcome.txt`
Contains the welcome message displayed when the program starts.

**Sample Content:**
```
Welcome to the Car Rental Management System!
Your journey to convenience starts here.
```

### `thanks.txt`
Contains a thank-you message displayed after the invoice is generated.

**Sample Content:**
```
Thank you for using our car rental services. We hope to see you again soon!
```

### `Toyota.txt`
Specifications for the Toyota 2021 model:
```
Specifications:

40 kWh and 60 kWh
Range                  EPA: 139 mi 224 km    EPA: 210 mi 340 km
Max. power, motor      382 hp 285 kW        382 hp 285 kW
Max. power, battery    235 hp 175 kW        302 hp 225 kW
```

### `Hyundai.txt`
Specifications for the Hyundai 2019 model:
```
Specifications:

80 kWh and 90 kWh
Range                  EPA: 139 mi 224 km    EPA: 210 mi 340 km
Max. power, motor      302 hp 285 kW        562 hp 285 kW
Max. power, battery    265 hp 175 kW        902 hp 225 kW
```

### `Ford.txt`
Specifications for the Ford 2020 model:
```
Specifications:

50 kWh and 80 kWh
Range                  EPA: 139 mi 224 km    EPA: 210 mi 340 km
Max. power, motor      682 hp 285 kW        682 hp 285 kW
Max. power, battery    935 hp 175 kW        802 hp 225 kW
```

---

## Concepts of OOP Used

### 1. **Classes and Objects**
- The program uses two classes:
  - `Customer`: Stores customer-related data.
  - `Rent`: Inherits from `Customer` and implements additional functionalities.

### 2. **Inheritance**
- `Rent` is a derived class inheriting the properties of the `Customer` base class.

### 3. **Encapsulation**
- Data members of the classes are declared as private or protected to restrict direct access.
- Public methods are provided to manipulate the data.

### 4. **Abstraction**
- The complexity of file reading, calculations, and data management is hidden behind well-defined methods.

---

## How to Run the Program

1. **Prerequisites:**
   - C++ compiler (e.g., g++).
   - All required text files (`welcome.txt`, `thanks.txt`, `Toyota.txt`, `Hyundai.txt`, `Ford.txt`) in the same directory as the source code.

2. **Compile the Program:**
   ```
   g++ car_rental.cpp -o car_rental
   ```

3. **Run the Program:**
   ```
   ./car_rental
   ```

---

## Future Enhancements
- Add more car models with detailed specifications.
- Implement a graphical user interface (GUI) for better user experience.
- Add a database to store and retrieve customer records.
- Include payment gateway integration for online transactions.

