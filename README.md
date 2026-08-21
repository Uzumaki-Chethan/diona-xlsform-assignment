# 🧾 Diona XLSForm Assignment

## 📌 Overview

This project presents an **ODK XLSForm implementation** of the *Criminal Risk Assessment Request* document.

The objective was to accurately replicate the original PDF form while enhancing it with **structured design, validation logic, and improved usability** using XLSForm standards.

XLSForm is a spreadsheet-based form standard used to design complex data collection forms in tools like ODK. :contentReference[oaicite:0]{index=0}

---

## 🎯 Objectives

- Convert a real-world PDF form into a digital XLSForm
- Maintain structural and logical consistency with the original document
- Improve data quality through validation and constraints
- Ensure user-friendly navigation using grouping and layout techniques

---

## 🧱 Form Structure

The form is organized into the following logical sections:

### 1. Consent Section
- Captures user consent status
- Includes conditional logic for witness/signature fields

### 2. Personal Information
- First Name, Second Name, Last Name
- Date of Birth and Gender
- Additional alias/name fields

### 3. Contact Information
- Address
- Phone number(s)
- City/Province/Country of Birth

### 4. Identification Details
- Multiple ID selection (Birth Certificate, Health Card, etc.)
- Constraint ensures **minimum 2 IDs are selected**

### 5. Criminal Risk Assessment Details
- Agency Name
- Reason for Risk Assessment
- Assigned Worker
- Submission details (Designate info, request date)

---

## ⚙️ Key Features & Implementation

### ✅ 1. Required Field Enforcement
All mandatory fields (marked with `*` in the original document) are enforced using:
required = yes

✅ 2. Validation Logic (Constraint)

A constraint ensures at least two identification proofs are selected:

count-selected(.) >= 2

This improves data accuracy and completeness.

✅ 3. Conditional Logic (Relevance)

Fields are shown dynamically based on user input using relevance expressions:

${consent_status} = 'consented'

This ensures:

Cleaner UI
Reduced unnecessary inputs
Better user experience
✅ 4. Grouping for Structure

The form uses begin_group and end_group to organize sections logically.

This improves:

Readability
Navigation
Professional layout
✅ 5. Clean Naming Conventions
All variables use snake_case
Names are consistent and meaningful
Avoids conflicts and improves maintainability
🧪 Testing & Validation

The form was tested using:

XLSForm Online Validator
Enketo Preview

Validation checks performed:

Required fields enforcement
Constraint validation (ID selection)
Logical flow of form
Error handling
🎥 Demo Video

🔗 Video uploaded to drive : https://drive.google.com/file/d/1AsXXewwV_008tHHMzCcynho6doA-kt1e/view?usp=sharing

The video demonstrates:

Form structure
Validation behavior
Functional walkthrough
📁 Repository Structure
diona-xlsform-assignment/
│
├── form.xlsx        # Main XLSForm file
├── README.md        # Project documentation
🛠️ Tools & Technologies Used
ODK XLSForm
Microsoft Excel
XLSForm Online Validator
Enketo Web Preview
📚 Concepts Used
Survey & Choices Sheet Structure
Question Types (text, select_one, select_multiple)
Constraints & Validation Logic
Relevance (Conditional Display)
Grouping (begin_group / end_group)
💡 Key Learnings
Translating static documents into dynamic digital forms
Applying validation to improve data quality
Structuring forms for usability and clarity
Implementing logic using XLSForm expressions
👤 Author

Chethan TD
