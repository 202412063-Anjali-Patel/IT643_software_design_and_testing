# Concepts in QuickMart | Multi-vendor E-commerce System

This document lists all the important concepts used in the "QuickMart", multi-vendor e-commerce project (which i have done in my bachelor studies). Each concept is divided into Object, Context, and information.

---

## 1. customer

### ➤ Context: as an unregistered user
- **Information (for registration)**:
  - name
  - email
  - password
  - is_active
  - created_at and updated_at  

### ➤ Context: as a registered user
- **Information (for login)**:
  - email
  - password  

### ➤ Context: while browsing products
- **Information (for giving similar products, ads or sale notifications)**:
  - viewed product name  
  - price
  - category 
  - brand 

### ➤ Context: while placing an order
- **Information (to make an order)**:
  - selected products details  
  - delivery address  
  - phone number and alternative phone number
  - payment method  
  - applied discount or coupon  
  - order notes  
  - order date

### ➤ Context: while tracking an order
- **Information**:
  - order id  
  - current status  
  - estimated delivery time  
  - delivery person details 

### ➤ Context: while delivering an order
- **Information (to authenticated a reciever person)**:
  - order id  
  - customer contact info
  - otp for verification

### ➤ Context: giving product review
- **Information**:
  - rating (1 to 5 stars)  
  - review text  
  - review date  
  - product id  

### ➤ Context: while managing platform customers
- **Information**:
  - customer id  
  - name  
  - registration date  
  - performance
  - status (active, blocked)
  
---

## 2. seller

### ➤ Context: as an unregistered user
- **Information (for registration)**:
  - name
  - email 
  - phone number
  - username
  - password
  - is_active
  - created_at and updated_at

### ➤ Context: as a registered user
- **Information (for login)**:
  - email
  - username
  - password  

### ➤ Context: while making business profile
- **Information**:
  - business name
  - business type
  - business strength
  - business description
  - business address (home address if business address is na)
  - product category
  - gst number
  - bank name
  - bank branch
  - bank ifsc code
  - bank account holder name
  - account number and type
  - proof of bank account ownership

### ➤ Context: while uploading products
- **Information**:
  - product name  
  - product brand
  - product category
  - product title
  - product description
  - product price
  - discount price
  - product quantity
  - product keywords
  - product color
  - product size and weigth (if needed)
  - product status (active | inactive)
  - product thumbnail image
  - product other images
  - created_at and updated_at

### ➤ Context: while monitoring product approvals
- **Information**:
  - product id  
  - seller id  
  - category  
  - approval status  
  - rejection reason (if any)

### ➤ Context: while processing orders
- **Information**:
  - order id  
  - product quantity  
  - shipping address  
  - expected dispatch date  
  - payment status

### ➤ Context: while checking performance of that particular seller
- **Information**:
  - total sales  
  - top-selling products  
  - customer reviews  
  - return ratio 
  - monthly revenue  

### ➤ Context: while managing platform sellers
- **Information**:
  - seller id  
  - name  
  - registration date  
  - performance
  - status (active, blocked) 

---

## 3. admin

### ➤ Context: as a user try to logged in
- **Information**:
  - email
  - username
  - password 

### ➤ Context: managing platform access
- **Information**:
  - access assigned to that admin  

---

## 4. overall system as an object

### ➤ Context: while tracking overall platform activity
- **Information**:
  - total orders  
  - active users  
  - daily revenue  
  - complaint reports  
  - error logs  

### ➤ Context: handling disputes
- **Information**:
  - order id  
  - customer/seller ids  
  - dispute description  
  - chat/message logs  
  - resolution status  

---

## 4. delivery person

### ➤ Context: as an applicant
- **Information**:
  - name
  - email
  - phone number
  - address
  - gender
  - date of birth
  - identity proof
  - vehicle details (type, rc book, puc, licence, insurance) 
  - experience details (if any)

### ➤ Context: as an approved user (system will provide username and password to that applicant after successful selection process and registration)
- **Information (in order to register that person as a delivery person)**:
  - name
  - email
  - phone number
  - address
  - gender
  - date of birth
  - identity proof
  - vehicle details (type, rc book, puc, licence, insurance) 
  - experience details (if any)
  - username
  - password
  - shift timing / working hours
  - salary 
  - job type
  - job responsibilities
  - terms and coditions for job
  - date
  - is_active

### ➤ Context: as an registered user
- **Information (in order to login)**:
  - email
  - username
  - password

### ➤ Context: while assigning a delivery
- **Information**:
  - availability
  - location
  - pending deliveries
  - vehicle capacity

### ➤ Context: while viewing assigned deliveries
- **Information**:
  - order id  
  - pickup address  
  - drop address  
  - contact of customer  
  - delivery deadline  

### ➤ Context: while updating delivery status
- **Information**:
  - order id  
  - delivery status (out for delivery, delivered, failed)  
  - timestamp  
  - remarks (optional)

### ➤ Context: while making payment
- **Information**:
  - bank name
  - bank branch
  - bank ifsc code
  - bank account holder name
  - account number and type
  - proof of bank account ownership  
  - amount to pay
  - payment method
  - date

### ➤ Context: while checking performance of that particular delivery person
- **Information**:
  - total delivery (successful and failed)
  - customer reviews

### ➤ Context: while managing platform delivery persons
- **Information**:
  - delivery person id  
  - name  
  - registration date  
  - performance
  - status (active, blocked)

---

## 5. employee

### ➤ Context: as an applicant
- **Information**:
  - name
  - email
  - phone number
  - address
  - gender
  - date of birth
  - identity proof
  - 12th marksheet
  - other education details (if any)
  - experience details (if any)

### ➤ Context: as an approved user (system will provide username and password to that applicant after successful selection process and registration)
- **Information (in order to register that person as an employee)**:
  - name
  - email
  - phone number
  - address
  - gender
  - date of birth
  - identity proof
  - 12th marksheet
  - other education details (if any)
  - experience details (if any)
  - username
  - password
  - shift timing / working hours
  - salary 
  - job type
  - job responsibilities
  - terms and conditions for job
  - date
  - is_active

### ➤ Context: as an registered user
- **Information (in order to login)**:
  - email
  - username
  - password

### ➤ Context: while managing inventory (if role assigned)
- **Information**:
  - access assigned to that employee

### ➤ Context: while making payment
- **Information**:
  - bank name
  - bank branch
  - bank ifsc code
  - bank account holder name
  - account number and type
  - proof of bank account ownership  
  - amount to pay
  - payment method
  - date

### ➤ Context: while managing platform employees
- **Information**:
  - employee id  
  - name  
  - registration date  
  - performance
  - status (active, blocked)
  
---

## 6. product review

### ➤ Context: customer gives review after delivery
- **Information**:
  - customer id  
  - product id  
  - rating (1 to 5 stars)  
  - review text  
  - review images (optional)  
  - review date  
  - verified purchase (yes or no)  

### ➤ Context: admin monitors reviews
- **Information**:
  - review id  
  - product id  
  - customer id  
  - review content  
  - rating  
  - flagged status (if reported)  
  - moderation status (approved, rejected, pending)  

### ➤ Context: display reviews on product page
- **Information**:
  - average rating  
  - total number of reviews  
  - most helpful review  
  - most recent review  
  - rating breakdown

---

## 7. cart

### ➤ Context: customer adds product to cart
- **Information**:
  - customer id  
  - product id  
  - selected quantity  
  - selected size, color (if applicable)  
  - date added  
  - cart item id  

### ➤ Context: customer views cart
- **Information**:
  - product details (name, image, price, discount, seller)  
  - subtotal for each item  
  - total price of all items  
  - estimated delivery date  
  - applied coupon (if any)

### ➤ Context: customer removes or updates cart items
- **Information**:
  - cart item id  
  - updated quantity or removed item  
  - timestamp of change  

---

## 8. wishlist

### ➤ Context: customer adds product to wishlist
- **Information**:
  - customer id  
  - product id  
  - product name  
  - product image  
  - product price  
  - date added  

### ➤ Context: customer views wishlist
- **Information**:
  - all saved product details  
  - availability status  
  - discount or price drop 

### ➤ Context: admin analyzes popular wishlist items
- **Information**:
  - most wished products  
  - total number of wishlists a product is in  
  - wishlist trends by category  

---

## 9. shared / other entities

### ➤ object: product  
- **used by**: customer, seller, admin  
- **contextual info**:
  - seller id
  - product name  
  - product brand
  - product category
  - product title
  - product description
  - product price
  - discount price
  - product quantity
  - product keywords
  - product color
  - product size and weigth (if needed)
  - product status (active | inactive)
  - product thumbnail image
  - product other images
  - created_at and updated_at
  - ratings
  - stock  

### ➤ object: order  
- **used by**: customer, seller, delivery person, admin  
- **contextual info**:
  - order id
  - product list
  - status
  - delivery address  
  - phone number and alternative phone number
  - payment status
  - payment method  
  - applied discount or coupon  
  - order notes  
  - order date
  - order total amount
  - delivery otp
  - order status
  - estimated delivery date

---
