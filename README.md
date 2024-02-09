<div align="center">

![][views] ![][stars] ![][forks] ![][issues] ![][license] ![][repo-size]

# magadh-bookstore-api

</div>

## 🛠️ Getting Started

⬇️ **Fetch latest source code from master branch.**

```bash
git clone https://github.com/Khushal-ag/magadh-bookstore.git

cd magadh-bookstore
```

🚧 **Create `.env` file & add your own `ENV_VARIABLES` as mentioned in `.env.example` file.**

```bash
PORT=3000
SKIP_ENV_VALIDATION=false

DATABASE_NAME=magadh_bookstore
DATABASE_URL= <YOUR_DATABASE_URL>

JWT_SECRET= <YOUR_JWT_SECRET>
```

💻 **To install dependencies:**

```bash
pnpm i
```

💻 **To install dependencies:**

```bash
pnpm dev
```

## For computing sellcount

The logic for computing the **sellCount** is the provided in **buyBook** function which involves updating the sellCount property of a book in the database. Here's how the logic works:

- The function retrieves the book information from the database based on the provided **_id_**.

- If the book is not found, it throws a custom error indicating that the book was not found.

- It then updates the **_sellCount_** property of the book. The quantity parameter is an optional parameter representing the number of books being purchased. If quantity is provided, it adds the quantity to the current **_sellCount_**. If quantity is not provided (i.e., it's undefined), it defaults to adding **1** to the **_sellCount_**. This ensures that the **_sellCount_** is incremented by **1** for each purchase by default.

- Finally, it updates the book's information in the database with the new **_sellCount_** value and returns the updated book object.

The logic assumes that each purchase, regardless of the quantity, increments the **_sellCount_** by **1**. If you uncomment the code block responsible for updating the stock based on the quantity purchased, you can adjust the sellCount and stock accordingly based on the quantity purchased. However, in the provided code, the focus is primarily on updating the sellCount.

## Reason for choosing the respective database design

Using Supabase with the Drizzle ORM for my database design and implementation offers several advantages and involves specific choices:

- **Supabase:** Supabase is an open-source Firebase alternative that provides real-time database capabilities, authentication, file storage, and more. Choosing Supabase as your backend platform offers scalability, reliability, and ease of use. Its integration with PostgreSQL ensures powerful relational database capabilities.

- **Drizzle ORM:** Drizzle ORM is an Object-Relational Mapping library designed specifically for Supabase. It simplifies database interactions by allowing developers to work with JavaScript objects instead of writing raw SQL queries. Drizzle ORM abstracts away the complexities of database operations, making development more efficient and less error-prone.

- **Database Schema Design:** When designing your database schema, you likely considered the entities and relationships relevant to your application domain. Supabase's support for PostgreSQL's relational features allows you to define tables, columns, constraints, and relationships to model your data effectively. You might have structured your schema to represent entities such as users, books, orders, transactions, etc., along with their attributes and relationships.

- **Normalization:** Normalization is an essential concept in relational database design aimed at reducing data redundancy and improving data integrity. With Supabase and Drizzle ORM, you can enforce normalization rules by defining tables with appropriate primary keys, foreign keys, and normalization forms. This ensures efficient storage utilization and minimizes update anomalies.

- **Data Integrity Constraints:** Utilizing data integrity constraints such as primary keys, foreign keys, unique constraints, and check constraints ensures data consistency and accuracy. With Supabase and Drizzle ORM, you can define these constraints at the schema level, enforcing rules that govern data integrity and preventing invalid data from entering the database.

- **Indexing and Performance:** Efficient querying is crucial for performance in database-driven applications. Supabase allows you to create indexes on columns frequently used in search conditions to speed up query execution. Drizzle ORM abstracts index creation and utilization, making it easier to optimize database performance without delving into low-level implementation details.

- **Real-time Capabilities:** Supabase's real-time capabilities enable live updates and synchronization between clients and the database. By leveraging features such as real-time listeners and subscriptions, you can build reactive applications that reflect database changes in real-time without polling or manual refreshes.

Overall, the choice of Supabase with Drizzle ORM for my database design and implementation reflects a commitment to leveraging modern tools and technologies to build scalable, efficient, and feature-rich applications while minimizing development overhead and complexity.

<!----------------------------------{ Labels }--------------------------------->

[views]: https://komarev.com/ghpvc/?username=magadh-bookstore&label=view%20counter&color=red&style=flat
[repo-size]: https://img.shields.io/github/repo-size/Khushal-ag/magadh-bookstore
[issues]: https://img.shields.io/github/issues-raw/Khushal-ag/magadh-bookstore
[license]: https://img.shields.io/github/license/Khushal-ag/magadh-bookstore
[forks]: https://img.shields.io/github/forks/Khushal-ag/magadh-bookstore?style=flat
[stars]: https://img.shields.io/github/stars/Khushal-ag/magadh-bookstore
