# Using-Entity-Framework-with-SQLite
20487_MOD02_DEMO_L4

Demonstration: Using Entity Framework with SQLite

Demonstration Steps

1. Open the Command Prompt window.
2. To change the directory to the starter project, at the command prompt, run the following command:
        cd [Repository Root]\AllFiles\Mod02\DemoFiles\Sqlite\Starter\Sqlite.Dal.Test
3. To use Entity Framework Core SQLite, install the following package from the command prompt:
        dotnet add package Microsoft.EntityFrameworkCore.Sqlite --version=2.1.1
4. To restore all the dependencies and tools of a project, at the command prompt, run the following command:
        dotnet restore
5. Move to the solution folder, paste the following command, and then press Enter:
        cd ..
6. Open the solution in VS Code, paste the following command, and then press Enter:
        code .
7. Expand Sqlite.Dal.Test, and then click DBSqliteTest.
8. Add the following property to the class:
         private DbContextOptions<SchoolContext> _options =
                    new DbContextOptionsBuilder<SchoolContext>()
                        .UseSqlite(@"Data Source = [Repository Root]\AllFiles\Mod02\DemoFiles\SQLite\Database\SqliteSchool.db")
                        .Options;
9. Switch to the Command Prompt window. To change directory to the Sqlite.Dal.Test project, at the command prompt, run the following command:
       cd Sqlite.Dal.Test
10. To run the all the test methods, paste the following command, and then press Enter:
         dotnet test
         
![20487D_Images](https://github.com/ialcaidef/Using-Entity-Framework-with-SQLite/blob/master/Sqlite.Dal.Test/01.png)

11. Open DB Browser for SQLite.
12. On the menu bar, click File, and then click Open Database.
13. In the Choose a database file window, browse to [Repository Root]\AllFiles\Mod02\DemoFiles\SQLite\Database, and then double-click SqliteSchool.db.
14. In the Database Structure tab, expand Tables.

![20487D_Images](https://github.com/ialcaidef/Using-Entity-Framework-with-SQLite/blob/master/Sqlite.Dal.Test/02.png)
15. Right-click the Persons table, and then select Browse Table.
16. In the Browse Data tab, verify that the student record Kari Hensien is in the database.
17. Close all open windows.
