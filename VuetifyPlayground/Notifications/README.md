# Notifications Component

## Overview
The **Notification** component consists of a **3-row, 3-column** layout, following **Vuetify standards (2x8x2 columns)**. It adapts between two sizes:
- **Collapsed:** 380x140 pixels
- **Expanded:** 380x210 pixels

## Layout Structure

### **Row 1:**
- **Column 2:** Title
- **Column 3:** Dismiss button

### **Row 2:**
- **Column 1:** Icon (with or without badge) or process circular indicator
- **Column 2:** Description or progress bar
- **Column 3:** Read/unread button

### **Row 3:**
- **Column 2:** Button area
- **Column 3:** Timestamp

## Themes & Styling
The component supports both **light** and **dark** themes with predefined colors:

### **Light Theme:**
- Background color: `#F3F3F3`
- Font color: `#9E9E9E`
- Component colors: `#9E9E9E`

### **Dark Theme:**
- Background color: `#757575`
- Font color: `#FFFFFF`
- Component colors: `#FFFFFF`

### **Additional Colors (Company-defined):**
- Light theme circular progress bar: `#361D5C`
- Dark theme circular progress bar: `#5C4582`
- Success: `#02A481`
- Error: `#C43633`
- Cancel: `#BCB9BF`
- Font family: **Segoe UI**

## Guidelines
To ensure consistency, follow these best practices when using notifications:

1. **Title Formatting:**
   - Use a **noun phrase** for new notifications (e.g., *Solution creation*).
   - Use **past participle** for completed tasks (e.g., *Solution created*).
2. **Descriptions** should be as detailed as possible.
3. **Button Labels** should not be excessively long.
4. **Timestamp Format:**
   - Use **hours** if the notification was created on the same day.
   - Use `#d` format if the notification was created **days ago**.
5. **Process Steps:**
   - A notification **cannot exceed 5 steps**.

## Notification DTO
The **Notification DTO** manages notifications using JSON properties:

| Property   | Description |
|------------|-------------|
| **StartTitle** (*) | Title shown when the notification is created. |
| **EndTitle** (*) | Title shown when the associated task completes. |
| **Icon** (*) | Icon representing the task that triggered the notification. |
| **Badge** | Optional badge to enhance process description. |

**(*) Mandatory fields**

