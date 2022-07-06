# VET CLINIC
> Vet clinic project based on the POSTGRE SQL DATABASE (STRUCTURED);
> It is used to store animals history profile in a vet clinic hospital;


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



![Screenshot 1443-12-06 at 17 38 19](https://user-images.githubusercontent.com/61976324/177379138-7b9f0ea1-caf0-4daa-ae00-4fabfdd3dbc4.png)

![Screenshot 1443-12-06 at 17 37 59](https://user-images.githubusercontent.com/61976324/177379283-c69953a9-3732-4cd8-98f0-c1831255f838.png)

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
