![TinyORM](TinyORM-Logo.png "TinyORM")

**TinyORM** by [Stan Drapkin](https://github.com/sdrapkin "Stan Drapkin") [sdrapkin at sdprime dot com]

## Features: ##
1.  Focused on **SQL Server** (any `SqlClient`-based db engine).
2.  **Intuitive, tiny, simple API**. This is the hardest part of any library to get right.
3.  **Does not obscure or reinvent `T-SQL`**. If you prefer APIs that hide `T-SQL` incompetence, [gtfo](https://en.wikipedia.org/wiki/Entity_Framework).
4.  **Very fast.** As fast as competition (`Dapper`, `OrmLite`, `PetaPoco`, `Linq2Sql`, etc. [benchmarks](https://gist.github.com/anonymous/86fdb2130071dbdad8211007346f3f96)). 
5.  **Seamlessly transactional** and safe. Transactions are not merely supported - they are the default. Custom transaction scopes are declared via standard `TransactionScope` instance (created via `TinyORM`.`DbContext`.`CreateTransactionScope()` factory).
6.  **Transparent connection management**. One less thing to worry about and screw up. Never think about connections again.
7.  `Task`-based `async` API (ie. *the* API). All calls are buffered (focus on safety and fast connection release).
8.  **POCOs** or `anonymous` objects are fine. No inheritance, interface, or attribute requirements.
9.   Returns `dynamic` entities which can also be consumed directly, or projected to statically-typed objects (fast!).
	* Either strict (perfect-match) or relaxed (best-effort) projection of `dynamic` to statically-typed objects.
10.  Full **parameterization**, with parameter list expansion (ex. `WHERE Id IN (@IdList)`). This also helps prevent SQL injection.
	* `CHAR`, `VARCHAR`, `NCHAR`, `NVARCHAR` support for `string` parameters. 
11. Single or multiple Result Sets.
12. **Snapshots** provide change-tracking, with `UPDATE` `T-SQL` generation for partial updates.
13. Intelligent **batched \*bulk\* command sequences** via `QueryBatch` (not just for `INSERT` - for all `CREATE/UPDATE/DELETE/MERGE` commands).
14. **Streaming data-out** support (ex. streaming out `BLOBs`/files).
15.  **Auditing**
	* Caller identity tracking (*which user made the call?*).
	* Callsite tracking (*which source code filename, method, and line# made the call?*).
16. Helpers for `CREATE`, `UPDATE`, `DELETE`, and `MERGE` `T-SQL` generation.
17. `SequentialGuid` generator for **fragmentation-free**, **unique**, **unguessable**, **code-generated** clustered `uniqueidentifier` indexes.
18. c# 6.0 in `safe` mode. Compiled `any cpu` for .NET 4.5.2+.
19. Tiny codebase. Tiny ~45k `.dll`. No dependencies.
20. `TinyORM` on [NuGet](https://www.nuget.org/packages/tinyorm) (`Install-Package TinyORM`).
21. **MS-PL** ([Microsoft Public](LICENSE.md)) license. If MS-PL does not suit you, contact me.

If you are serious about SQL Server, give **TinyORM** a try (even if you're a `Dapper` fan).

## ##
Nature graphic by [Freepik](http://www.flaticon.com/authors/freepik) is licensed under [CC BY 3.0](http://creativecommons.org/licenses/by/3.0/).