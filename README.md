# To repozytorium zawiera dokumentację również w języku polskim, która znajduje się poniżej.

# EN / Car Dealership Management – Python + MySQL

    A simple console-based application written in Python that connects to a remote MySQL database and simulates a car dealership management system.
    The program allows viewing, adding, editing and deleting cars stored in an online database.

# 📌 Overview

    This project demonstrates how to:
        •	Connect a Python application to a remote SQL server
        •	Execute SQL queries (SELECT, INSERT, UPDATE, DELETE)
        •	Build a simple CRUD system (Create / Read / Update / Delete)
        •	Interact with a structured database using a console interface

    The system imitates a basic car dealership where a user can manage cars available in the database.

# 🚀 Features

    1. View Cars
    
        •   Displays all vehicles stored in the samochody table.
    
    2. Add a Car

        Insert a new car into the database with validation for:
            •	production year (must be an integer)
            •	price (must be a number)

    3. Delete a Car
    
        •   Remove a car from the database by ID.

    4. Edit Car Data

        Update selected information:
            •	brand
            •	model
            •	production year
            •	price

    5. Console Menu
    
        •   A simple text-based menu for easy navigation.

# 📋 Requirements

## Functional Requirements
    •	Connect to a remote MySQL database
    •	Display all cars from the table
    •	Add new cars with validation
    •	Edit existing cars
    •	Delete cars
    •	Provide a console menu for navigation
    •	End connection safely after program exit

## Non-Functional Requirements
	•	Provide clear communication for invalid input
	•	Handle database connection errors gracefully
	•	Ensure input data types (int/float) are validated
	•	Keep the environment lightweight (Python + one package)
	•	Maintain code readability and modularity

# 🧩 How It Works (Architecture)

## 1. Database Structure

    The app expects a table:

    CREATE TABLE samochody (
        id INT AUTO_INCREMENT PRIMARY KEY,
        marka VARCHAR(255),
        model VARCHAR(255),
        rok_produkcji INT,
        cena DECIMAL(10,2)
    );

## 2. Database Connection

    The program uses mysql.connector to establish a connection with a remote MySQL database:

    polaczenie = mysql.connector.connect(
        host=hostname,
        database=database,
        user=username,
        password=password,
        port=port
    )

    If the connection (połączenie) succeeds, the program allows further operations; otherwise an error is displayed.

## 3. Database Operations (CRUD)

    The app includes the following functions:

    Function:           |      Purpose:
                        |
    pokaz_samochody()	|      Displays all rows from samochody (cars)
    dodaj_samochod()	|      Inserts a new row
    usun_samochod() 	|      Removes a row by ID
    edytuj_samochod()	|      Updates selected fields

    Each modification ends with commit() to save changes.

## 4. User Interface

    A simple loop shows the menu and executes user-selected options.

# 🛠 Technologies Used
	•	Python 3
	•	mysql-connector-python (database communication)
	•	Remote MySQL server (Filess.io in provided example)

**────────────────────────**

# 🇵🇱 Zarządzanie Salonem Samochodowym – Python + MySQL

    Prosta aplikacja konsolowa napisana w Pythonie, która łączy się ze zdalną bazą danych MySQL i symuluje system zarządzania salonem samochodowym.
    Program umożliwia wyświetlanie, dodawanie, edytowanie oraz usuwanie samochodów przechowywanych w bazie online.

# 📌 Opis ogólny

    Projekt demonstruje, jak:
        •	połączyć aplikację Python z zdalnym serwerem SQL,
        •	wykonywać zapytania SQL (SELECT, INSERT, UPDATE, DELETE),
        •	zbudować prosty system CRUD (Create / Read / Update / Delete),
        •	obsługiwać ustrukturyzowaną bazę danych za pomocą interfejsu konsolowego.

    System symuluje podstawowy salon samochodowy, w którym użytkownik może zarządzać autami dostępnymi w bazie.

# 🚀 Funkcje

    1. Wyświetlanie samochodów

        •	Pokazuje wszystkie pojazdy zapisane w tabeli samochody.

    2. Dodawanie nowego samochodu

        Dodaje nowe auto do bazy danych z walidacją:
            •	rok produkcji musi być liczbą całkowitą,
            •	cena musi być liczbą.

    3. Usuwanie samochodu

        •	Usuwa auto z bazy na podstawie jego ID.

    4. Edycja samochodu

        Można zaktualizować:
            •	markę,
            •	model,
            •	rok produkcji,
            •	cenę.

    5. Menu konsolowe

        •	Proste, czytelne menu tekstowe ułatwiające nawigację.


# 📋 Wymagania

## Wymagania funkcjonalne
	•	Połączenie ze zdalną bazą MySQL
	•	Wyświetlanie wszystkich samochodów z tabeli
	•	Dodawanie nowych pojazdów z walidacją danych
	•	Edytowanie istniejących samochodów
	•	Usuwanie samochodów
	•	Udostępnienie menu konsolowego
	•	Bezpieczne zakończenie połączenia z bazą przy wyjściu z programu

## Wymagania niefunkcjonalne
	•	Czytelne komunikaty przy błędnym wejściu
	•	Łagodna obsługa błędów związanych z bazą danych
	•	Walidacja typów danych (int/float)
	•	Lekkość środowiska (Python + 1 pakiet)
	•	Zachowanie czytelności i modularności kodu

#🧩 Jak to działa (Architektura)

## 1. Struktura bazy danych

    Aplikacja oczekuje tabeli:

    CREATE TABLE samochody (
        id INT AUTO_INCREMENT PRIMARY KEY,
        marka VARCHAR(255),
        model VARCHAR(255),
        rok_produkcji INT,
        cena DECIMAL(10,2)
    );

## 2. Połączenie z bazą danych

    Program używa mysql.connector do połączenia ze zdalnym serwerem MySQL:

    polaczenie = mysql.connector.connect(
        host=hostname,
        database=database,
        user=username,
        password=password,
        port=port
    )

    Jeśli połączenie powiedzie się, aplikacja umożliwia dalsze operacje; w przeciwnym razie wyświetlany jest komunikat o błędzie.

## 3. Operacje na bazie danych (CRUD)

    Aplikacja zawiera następujące funkcje:

    Funkcja:            |       Cel:
                        |
    pokaz_samochody()	|       Wyświetla wszystkie rekordy z tabeli
    dodaj_samochod()	|       Dodaje nowy rekord
    usun_samochod()	    |       Usuwa rekord na podstawie ID
    edytuj_samochod()	|       Aktualizuje wybrane pola w rekordzie

    Każda modyfikacja kończy się wywołaniem commit() w celu zapisania zmian.

## 4. Interfejs użytkownika

	Prosta pętla wyświetlająca menu i wykonująca wybrane przez użytkownika akcje.

# 🛠 Technologie
	•	Python 3
	•	mysql-connector-python – komunikacja z bazą danych
	•	Zdalny serwer MySQL (w przykładzie Filess.io)
