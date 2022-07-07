# VET CLINIC
> Vet clinic project based on the POSTGRE SQL DATABASE (STRUCTURED);
> It is used to store animals history profile in a vet clinic hospital;
> Use database transactions.
> Modify and delete data in SQL.
> Prepare complex queries that answer analytical questions.



## Getting Started

This repository includes files with plain SQL that can be used to recreate a database:

- Use [schema.sql](./schema.sql) to create all tables.
- Use [data.sql](./data.sql) to populate tables with sample data.
- Check [queries.sql](./queries.sql) for examples of queries that can be run on a newly created database. **Important note: this file might include queries that make changes in the database (e.g., remove records). Use them responsibly!**


- Open SQL Shell and perform the following query operations
> SELECT * FROM animals;
> SELECT * FROM animals WHERE date_of_birth BETWEEN '2016/01/01' AND '2019/12/31';
> SELECT * FROM animals WHERE neutered=true AND escape_attempts < 3;
> SELECT * FROM animals WHERE name='Agumon' OR name='Pikachu';
> SELECT date_of_birth FROM animals WHERE name='Agumon' OR name='Pikachu';
> SELECT name, escape_attempts FROM animals WHERE weight_kg > 10.5;
> SELECT * FROM animals WHERE neutered=true;
> SELECT * FROM animals WHERE name='Gabumon';
> SELECT * FROM animals WHERE NOT name='Gabumon';
> SELECT * FROM animals WHERE weight_kg BETWEEN 10.4 AND 17.3;

> BEGIN;

> ALTER TABLE animals ADD species VARCHAR(50);

> UPDATE animals SET species='unspecified';

> ROLLBACK;

> UPDATE animals SET species='pokemon' WHERE species IS NULL;

> BEGIN;

> DELETE FROM animals;

> ROLLBACK;

> DELETE FROM animals WHERE date_of_birth > '2022-01-01';

> BEGIN;

> SAVEPOINT savepoint_01;

> UPDATE animals SET weight_kg = weight_kg * -1;

> ROLLBACK TO SAVEPOINT savepoint_01;

> UPDATE animals SET weight_kg = weight_kg * -1 WHERE weight_kg < 0;

> COMMIT;

/* Also query the following operations */

> SELECT COUNT(*) FROM animals;

> SELECT COUNT(*) FROM animals WHERE escape_attempts = 0;

> SELECT AVG(weight_kg) FROM animals;

> SELECT neutered, AVG(escape_attempts) AS Avg_attempt_ascape FROM animals GROUP BY neutered;

> SELECT species, MIN(weight_kg), MAX(weight_kg) FROM animals GROUP BY species;

> SELECT species, AVG(escape_attempts) FROM animals WHERE date_of_birth BETWEEN '1990-01-01' AND '2000-12-31' GROUP BY species;


![Screenshot 1443-12-08 at 00 39 13](https://user-images.githubusercontent.com/61976324/177663840-16d07ceb-4176-4e55-95bd-1e09e9403701.png)

![Screenshot 1443-12-08 at 00 39 39](https://user-images.githubusercontent.com/61976324/177663928-2d49d98e-7f9e-4ae4-a238-ef419491b7c0.png)

![Screenshot 1443-12-08 at 01 06 18](https://user-images.githubusercontent.com/61976324/177664043-e058e1e1-ea41-40cb-b670-6c720d2f9a51.png)

![Screenshot 1443-12-08 at 01 06 33](https://user-images.githubusercontent.com/61976324/177664084-4487d280-b94c-4901-bc04-8a3014e4890b.png)

## Authors   

👤 **Author1**

**Oyelakin Ridwan Adio**
- GitHub: [@oyelakin](https://github.com/oyelakinG9)
- Twitter: [@oyelakin](https://twitter.com/OyelakinG1)
- LinkedIn: [@oyelakin](https://www.linkedin.com/in/oyelakin-ridwan-4b4a02b6/)

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Hat tip to anyone whose code was used
- Inspiration
- etc

## 📝 License

This project is [MIT](./MIT.md) licensed.
