# Database Biblioteca

## Books <!-- Prima Entità -->

- id: PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- title: VARCHAR(50) NOTNULL INDEX <!-- Index serve per velocizzare la ricerca -->
- plot: TEXT NULL
- pages: SMALLINT NULL
- year: YEAR NULL
- cover_image: VARCHAR(255), NULL

---

- avaibility:
- price:
- online_content:
- discount:
- bestseller:
- language:
- chapters:
- edition:
- new_release:
- rarity:
- quantity:

## Copies <!-- Delle copie dell'entità -->

- id : PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- ean : VARCHAR(16) NULL
- isbn: VARCHAR(13) NULL
- position : VARCHAR(15) NULL
- language : VARCHAR(5) NULL DEFAULT("it-IT")

## Users <!-- A chi prestiamo questi libri -->

- id: PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- name: VARCHAR(50) NOTNULL
- lastname: VARCHAR(50) NOTNULL
- age: TINYINT NOTNULL
- email: VARCHAR(50) NOTNULL UNIQUE
- address: VARCHAR(40) NULL
- tel_number: VARCHAR(15) NULL

## Loans <!-- Prestito -->

- id: PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- start_date : DATETIME NOTNULL
- end_date: DATETIME NOTNULL

## Genres <!-- Generi del libro -->

- id: PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- name: VARCHAR(20) NOTNULL INDEX

## Authors <!-- Autori del libro -->

- id: PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- name: VARCHAR(50) NOTNULL
- lastname: VARCHAR(50) NOTNULL
- nationality: VARCHAR(20) NULL

## Publishers <!-- Le case editrici -->

- id: PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- name: VARCHAR(50) NOTNULL

## Conditions <!-- Condizioni del libro -->

- id : PK, NOTNULL, INDEX, UNIQUE, AUTOINCREMENTAL
- name : VARCHAR(50) NOTNULL
