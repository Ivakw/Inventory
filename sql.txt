
CREATE TABLE `inventory`.`suppliers` (
  `SupplierId` INT NOT NULL,
  `CompanyName` VARCHAR(45) NOT NULL,
  `ContactFName` VARCHAR(45) NOT NULL,
  `ContactLName` VARCHAR(45) NOT NULL,
  `Address1` VARCHAR(100) NOT NULL,
  `Address2` VARCHAR(100) NULL,
  `City` VARCHAR(45) NOT NULL,
  `PostalCode` INT NULL,
  `Country` VARCHAR(45) NOT NULL,
  `Phone` INT NOT NULL,
  `Email` VARCHAR(45) NOT NULL,
  `PaymentMethod` VARCHAR(45) NULL,
  PRIMARY KEY (`SupplierId`));

CREATE TABLE `inventory`.`products` (
  `ProductId` INT NOT NULL,
  `SKU` INT NOT NULL,
  `ProductName` VARCHAR(45) NOT NULL,
  `ProductDescription` VARCHAR(45) NOT NULL,
  `SupplierId` INT NOT NULL,
  `CategoryId` INT NULL,
  `UnitPrice` VARCHAR(45) NULL,
  `MaxRetailPrice` VARCHAR(45) NULL,
  `ReorderLevel` VARCHAR(45) NULL,
  PRIMARY KEY (`ProductId`));


CREATE TABLE `inventory`.`products` (
  `CategoryId` INT NOT NULL,
  `CategoryName` VARCHAR(45) NOT NULL,
  `Description` VARCHAR(45) NOT NULL,
  `Status` VARCHAR(10) NOT NULL,
  PRIMARY KEY (`CategoryId`));


CREATE TABLE `inventory`.`orders` (
  `OrderId` INT NOT NULL,
  `CustomerId` INT NOT NULL,
  `OrderNumber` VARCHAR(45) NOT NULL,
  `PaymentId` VARCHAR(45) NOT NULL,
  `OrderDate` INT NOT NULL,
  `ShippingDate` INT NULL,
  `ShippingId` VARCHAR(45) NULL,
  `PaymentDate` VARCHAR(45) NULL,
  PRIMARY KEY (`OrderId`));


CREATE TABLE `inventory`.`order_details` (
  `OrderId` INT NOT NULL,
  `ProductId` INT NOT NULL,
  `OrderNumber` INT NOT NULL,
  `Price` VARCHAR(10) NOT NULL,
  `Qty` INT NOT NULL,
  `Discount` INT NULL,
  `Total` VARCHAR(45) NULL,
  `ShipDate` DATE NULL,
  `BillDate` DATE NULL,
  PRIMARY KEY (`OrderId`));


CREATE TABLE `inventory`.`shippers` (
  `ShipperId` INT NOT NULL,
  `CompanyName` VARCHAR(30) NOT NULL,
  `Phone` INT NOT NULL,
  `email` VARCHAR(10) NOT NULL,
  PRIMARY KEY (`ShipperId`));


CREATE TABLE `inventory`.`customers` (
  `CustomerId` INT NOT NULL,
  `FName` VARCHAR(30) NOT NULL,
  `LName` VARCHAR(30) NOT NULL,
  `Address1` VARCHAR(10) NOT NULL,
  `Address2` VARCHAR(45) NULL,
  `City` VARCHAR(45) NULL,
  `State` VARCHAR(45) NULL,
  `PostalCode` INT NULL,
  `Country` VARCHAR(25) NULL,
  `Phone` INT NULL,
  `Email` VARCHAR(30) NULL,
  PRIMARY KEY (`CustomerId`));

