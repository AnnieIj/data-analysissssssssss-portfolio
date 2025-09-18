-- ========================================
-- Database: StoreDB
-- ========================================
-- Create Customers table
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    FirstName VARCHAR(50),
    LastName VARCHAR(50),
    Email VARCHAR(100),
    Phone VARCHAR(20),
    City VARCHAR(50),
    Country VARCHAR(50)
);

-- Insert data into Customers
INSERT INTO Customers (CustomerID, FirstName, LastName, Email, Phone, City, Country)
VALUES
(1, 'John', 'Doe', 'john.doe@email.com', '555-1234', 'Lagos', 'Nigeria'),
(2, 'Mary', 'Smith', 'mary.smith@email.com', '555-5678', 'Abuja', 'Nigeria'),
(3, 'Ahmed', 'Khan', 'ahmed.khan@email.com', '555-8765', 'London', 'UK'),
(4, 'Grace', 'Lee', 'grace.lee@email.com', '555-3456', 'Toronto', 'Canada'),
(5, 'Carlos', 'Santos', 'carlos.santos@email.com', '555-6543', 'Madrid', 'Spain');

-- ========================================
-- Create Products table
CREATE TABLE Products (
    ProductID INT PRIMARY KEY,
    ProductName VARCHAR(100),
    Category VARCHAR(50),
    Price DECIMAL(10,2),
    Stock INT
);

-- Insert data into Products
INSERT INTO Products (ProductID, ProductName, Category, Price, Stock)
VALUES
(1, 'Laptop', 'Electronics', 450000.00, 50),
(2, 'Smartphone', 'Electronics', 250000.00, 100),
(3, 'Desk Chair', 'Furniture', 75000.00, 30),
(4, 'Notebook', 'Stationery', 1500.00, 500),
(5, 'Headphones', 'Electronics', 35000.00, 80);

-- ========================================
-- Create Orders table
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    OrderDate DATE,
    TotalAmount DECIMAL(10,2),
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);

-- Insert data into Orders
INSERT INTO Orders (OrderID, CustomerID, OrderDate, TotalAmount)
VALUES
(1, 1, '2025-09-01', 450000.00),
(2, 2, '2025-09-02', 285000.00),
(3, 3, '2025-09-03', 76500.00),
(4, 4, '2025-09-05', 153000.00),
(5, 5, '2025-09-07', 250000.00);

-- ========================================
-- Create OrderDetails table
CREATE TABLE OrderDetails (
    OrderDetailID INT PRIMARY KEY,
    OrderID INT,
    ProductID INT,
    Quantity INT,
    Subtotal DECIMAL(10,2),
    FOREIGN KEY (OrderID) REFERENCES Orders(OrderID),
    FOREIGN KEY (ProductID) REFERENCES Products(ProductID)
);

-- Insert data into OrderDetails
INSERT INTO OrderDetails (OrderDetailID, OrderID, ProductID, Quantity, Subtotal)
VALUES
(1, 1, 1, 1, 450000.00), 
(2, 2, 2, 1, 250000.00),
(3, 2, 5, 1, 35000.00),
(4, 3, 3, 1, 75000.00),
(5, 3, 4, 1, 1500.00),
(6, 4, 2, 1, 250000.00),
(7, 4, 5, 1, 35000.00),
(8, 5, 2, 1, 250000.00);
