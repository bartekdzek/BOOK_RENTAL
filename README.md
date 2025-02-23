# 📚 Book Rental Application

## 📖 Table of Contents
- [📌 Project Overview](#-project-overview)
- [🛠️ Technologies Used](#-technologies-used)
- [✨ Features](#-features)
- [🏗️ Class Structure](#-class-structure)
- [🚀 Usage Guide](#-usage-guide)
- [👨‍💻 Authors](#-authors)

## 📌 Project Overview
This project is a **Book Rental Application** 📖 developed using **WPF (Windows Presentation Foundation)**.  
It allows users to manage a book rental system, enabling them to:
✔️ Browse books by category  
✔️ Borrow & return books  
✔️ Report lost books  
✔️ Sort & filter book lists  

The application keeps track of borrowed and lost books 📚 and calculates the total penalty cost 💰.

## 🛠️ Technologies Used
- 💻 **Programming Language:** C#
- 🏗️ **Framework:** .NET with WPF
- 📂 **Data Storage:** XML serialization
- 🎯 **Design Pattern:** Object-Oriented Programming (OOP)

## ✨ Features
🔎 **View Books** – Browse books by category or all available books  
📥 **Borrow Books** – Select a book and mark it as borrowed  
📤 **Return Books** – Move a borrowed book back to the available list  
❗ **Report Lost Books** – Mark a book as lost and calculate penalties  
📌 **Sorting & Filtering** – Sort books alphabetically and filter by category  
💾 **Data Persistence** – Save and load book data using XML  

## 🏗️ Class Structure

### 🔹 Main Classes
#### 📚 `Ksiazka` (Abstract Class)
Defines a book with attributes:
- `📖 Title`
- `✍️ Author`
- `📅 Publication Year`
- `🔢 ISBN`
- `💰 ObliczCene()` - Calculates the fine for lost books
- `📝 Clone()`, `⚖️ CompareTo()`, `✅ Equals()`

#### 🔸 Inherited Classes
- **👤 `Biografia`** – Adds `OsobaBiografia` to store the biography subject  
- **📘 `Encyklopedia`** – Includes `ZakresTematyczny` and `NumerTomu`, with a randomized fine  
- **📚 `Podrecznik`** – Represents textbooks with `Przedmiot` and `PoziomEdukacji`  
- **📖 `Poradnik`** – Guidebooks categorized via `EnumRodzajPoradnika`, with a fixed fine  
- **📕 `Powiesc`** – Represents novels, categorized by `RodzajLiteratury`  

#### 🏛️ `Biblioteka`
Manages book operations:
- 📂 **Lists:**  
  - `📚 wszystkieKsiazki` – All books  
  - `📖 dostepneKsiazki` – Available books  
  - `📕 wypozyczoneKsiazki` – Borrowed books  
  - `❌ zgubioneKsiazki` – Lost books  
- 🛠 **Operations:**  
  - `➕ DodajKsiazke()` – Add a book  
  - `📥 WypozyczKsiazke()` – Borrow a book  
  - `📤 ZwrocKsiazke()` – Return a book  
  - `🚨 ZglosZgube()` – Report a lost book  
  - `🔀 SortujKsiazki()` – Sort books  
  - **📂 XML-based** data saving/loading  

#### 🖥️ `MainWindow`
Handles UI interactions using WPF:
- 🎯 **Buttons & Events:**  
  - `📥 WypozyczButton_Click`
  - `📤 OddajButton_Click`
  - `🚨 ZglosButton_Click`
  - `🔠 AZButton_Click` (Sort)
- 📋 **List Handling:**  
  - `🔄 OdswiezListeKsiazek()`
  - `🔽 ComboBox_SelectionChanged()`

## 🚀 Usage Guide

### ▶️ Running the Application
1. Open **`Projekt_GUI.sln`** in **Visual Studio** 🖥️  
2. Build and run the project 🏗️  

### 🛠 User Actions
#### 📥 **Borrowing a Book**
1. Select a book from the available list 📚  
2. Click **"Wypożycz"** ✅  

#### 📤 **Returning a Book**
1. Click **"Oddaj"** ↩️  
2. Enter the book's ISBN 🔢  

#### 🚨 **Reporting a Lost Book**
1. Click **"Zgłoś zgubę"** ❗  
2. Enter the ISBN 🔢  

#### 🔀 **Sorting & Filtering**
- **Sort alphabetically** 🔠: Click **"A-Z"**  
- **Filter by category** 📂: Use the dropdown menu  

## 👨‍💻 Authors
- **🛠 Bartosz Tasak** – Abstract `Ksiazka` class, inherited classes (`Biografia`, `Encyklopedia`, `Podrecznik`, `Poradnik`, `Powiesc`), `KsiazkaException`  
- **🎨 Tomasz Profic** – Graphical user interface (WPF)  
- **🏗️ Kacper Urbański** – `Biblioteka` class, `Program`, UML diagram  

---

🚀 *This project is a final assignment for the **Object-Oriented Programming** course (Academic Year 2024/2025).*  
