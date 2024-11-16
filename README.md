# 🌌 Universe Database Project 🚀

**Version:** 1.0.0  
**Author:** Niladri Das
**Date:** 15.11.2024  
**License:** MIT

## 📜 Introduction

Welcome, intrepid explorer, to the Universe Database Project! This monumental endeavor encapsulates the vast and enigmatic cosmos within the confines of a PostgreSQL database. Herein lies a meticulously crafted schema that organizes celestial bodies, galaxies, and cosmic phenomena into a harmonious digital symphony. Prepare to embark on an interstellar journey through data!

## 🚀 Table of Contents

- [Project Overview](#project-overview)
- [Database Schema](#-database-schema)
- [Table Descriptions](#️-table-descriptions)
- [Installation Instructions](#️-installation-instructions)
- [Usage](#-usage)
- [Data Insertion](#-data-insertion)
- [Contributing](#-contributing)
- [License](#-license)

## 🌌 Project Overview

The Universe Database is a celestial repository that encapsulates the grandeur of the cosmos. With tables dedicated to galaxies, stars, planets, moons, and even black holes, this database serves as a comprehensive archive of astronomical knowledge. Each table is a veritable treasure trove of information, meticulously designed to facilitate queries that traverse the cosmic expanse.

## 📊 Database Schema

The database consists of the following illustrious tables:

- **galaxy:** A repository of galaxies, each with its own unique characteristics and attributes.
- **star:** Capturing the brilliance of stars, their ages, and their celestial homes.
- **planet:** Documenting the myriad planets that orbit these stars, revealing their potential for life.
- **moon:** A collection of moons that grace the planets, each with its own fascinating details.
- **black_hole:** A mysterious table dedicated to the enigmatic black holes that lurk in the depths of space.

## 🛠️ Table Descriptions

### Galaxy Table

- `galaxy_id:` A unique identifier for each galaxy (Primary Key).
- `name:` The dazzling name of the galaxy (Unique, Non-nullable).
- `description:` A textual description that captures the essence of the galaxy (Non-nullable).
- `distance_from_earth:` The distance of the galaxy from Earth in light-years (Numeric).
- `has_life:` A boolean indicator of whether life exists in the galaxy (Non-nullable).

### Star Table

- `star_id:` A unique identifier for each star (Primary Key).
- `name:` The illustrious name of the star (Unique, Non-nullable).
- `galaxy_id:` A foreign key referencing the galaxy to which the star belongs.
- `age_in_millions_of_years:` The age of the star measured in millions of years (Integer, Non-nullable).
- `is_spherical:` A boolean indicating whether the star is spherical in shape (Non-nullable).

### Planet Table

- `planet_id:` A unique identifier for each planet (Primary Key).
- `name:` The enchanting name of the planet (Unique, Non-nullable).
- `star_id:` A foreign key referencing the star that the planet orbits.
- `has_life:` A boolean indicating the potential for life on the planet (Non-nullable).
- `planet_types:` A textual description of the planet's classification (Non-nullable).
- `age_in_millions_of_years:` The planet's age in millions of years (Integer, Non-nullable).

### Moon Table

- `moon_id:` A unique identifier for each moon (Primary Key).
- `name:` The captivating name of the moon (Unique, Non-nullable).
- `planet_id:` A foreign key referencing the planet that the moon orbits.
- `has_life:` A boolean indicating whether life exists on the moon (Non-nullable).
- `distance_from_planet:` The distance of the moon from its parent planet in kilometers (Numeric, Non-nullable).

### Black Hole Table

- `black_hole_id:` A unique identifier for each black hole (Primary Key).
- `name:` The enigmatic name of the black hole (Unique, Non-nullable).
- `galaxy_id:` A foreign key referencing the galaxy where the black hole resides.
- `mass:` The mass of the black hole in solar masses (Numeric, Non-nullable).
- `has_event_horizon:` A boolean indicating the presence of an event horizon (Non-nullable).

## 🛠️ Installation Instructions

**Prerequisites:** Ensure that you have PostgreSQL installed on your machine. If not, visit the PostgreSQL official website for installation instructions.

**Clone the Repository:** Use the following command to clone the repository to your local machine:

```bash
git clone https://github.com/bniladridas/universe-database.git
```

## Navigate to the Project Directory:

```
cd universe-database
```

**Create the Database:** Open your PostgreSQL command line and execute:

```
CREATE DATABASE universe;
```

**Connect to the Database:**

```
\c universe;
```

**Run the SQL Script:** Execute the provided SQL script to create the tables and insert the data:

```
\i universe.sql
```

## 🌠 Usage

Once the database is set up, you can start querying the cosmos! Use SQL commands to explore the vastness of the universe stored within your database. Here are a few example queries to get you started:

**Retrieve all galaxies:**

```
SELECT * FROM galaxy;
```

**Find all stars in a specific galaxy:**

```
SELECT * FROM star WHERE galaxy_id = 1;
```

**List all planets that potentially harbor life:**

```
SELECT * FROM planet WHERE has_life = TRUE;
```

## 🌌 Data Insertion

To add more celestial bodies to your database, simply use the INSERT INTO command with the appropriate table. For example, to add a new star:

```
INSERT INTO star (name, galaxy_id, age_in_millions_of_years, is_spherical) VALUES ('New Star', 1, 100, TRUE);
```

## 🤝 Contributing
We welcome contributions from fellow cosmic enthusiasts! If you wish to enhance this project, please fork the repository and submit a pull request. Ensure that your code adheres to the cosmic coding standards and is well-documented.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](/LICENSE) file for details.

Thank you for embarking on this cosmic journey with the Universe Database Project! May your queries be swift and your discoveries profound! 🌌✨