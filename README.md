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


![Screenshot 1443-12-07 at 15 43 11](https://user-images.githubusercontent.com/61976324/177592622-fe3ec847-5dc1-4258-b1e1-af5b34e7f6af.png)

![Screenshot 1443-12-07 at 15 44 27](https://user-images.githubusercontent.com/61976324/177592945-ba0947c6-7129-48d6-b0cd-4c0c6621ba2e.png)

![Screenshot 1443-12-07 at 15 45 18](https://user-images.githubusercontent.com/61976324/177593250-9a098ff0-e6ea-406c-890b-2ff0e4848d72.png)

![Screenshot 1443-12-07 at 15 46 19](https://user-images.githubusercontent.com/61976324/177593476-d502661f-4f12-4bd1-b942-4caf5e97f8cb.png)

Also perfomed the following queries operation shown in below screenshot 


![Screenshot 1443-12-07 at 16 10 18](https://user-images.githubusercontent.com/61976324/177594113-796c96fa-47d4-47b3-8414-e9561afbc01d.png)

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
