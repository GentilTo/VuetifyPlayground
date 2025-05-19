# Notifications Component

## Overview
The **Notification** component consists of a **3-row, 3-column** layout, following **Vuetify standards (1x9x2 columns)**. It adapts between two sizes:
- **Collapsed:** 380x140 pixels
- **Expanded:** 380xAuto pixels

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
The component supports both **light** and **dark** themes with predefined colors.

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
   - Use a **noun phrase** for new notifications (e.g., *Creating new solution 123*).
   - Use **past participle** for completed tasks (e.g., *Solution 123 created*).
2. **Descriptions** should be as detailed as possible.
3. **Button Labels** should not be excessively long.
4. **Timestamp Format:**
   - Use **hours** if the notification was created on the same day.
   - Use `#d` format if the notification was created **days ago**.
5. **Process Steps:**
   - A notification can display the steps of a task. 

## Notification DTO
The way icons and badges are displayed in the **Notification DTO** is using the Icon property and the Badge JSON property:

| Property   | Description |
|------------|-------------|
| **Icon** (*) | Icon representing the task that triggered the notification. |
| **Badge** | Optional badge to enhance process description. |

**(*) Mandatory fields**

| Property   | Description |
|------------|-------------|
| **Icon** (*) | Icon representing the badge icon result (e.g. mdi-rocket). |
| **Color** | Optional badge to enhance process description (e.g. success). |
