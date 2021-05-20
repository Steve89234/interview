# Task \#3

This task will test your skills with SQL. This can be done conceptually but for your convenience if you would like to solve this task in practice, refer to the following statements to create the table and populate it with data:

```
CREATE TABLE task_3 (
    user_id INT(6) UNSIGNED NOT NULL,
    alias VARCHAR(255) NOT NULL,
    team_id INT(6) UNSIGNED NOT NULL
);
```

```
INSERT INTO task_3 VALUES
( 1, 'Robert', 1 ),
( 1, 'Bob', 2 ),
( 1, 'Bobby', 3 ),
( 2, 'Anna', 1 ),
( 2, 'Ann', 2 ),
( 2, 'Ann', 3 ),
( 2, 'Ann', 4 ),
( 3, 'Kathy', 1 ),
( 3, 'Kate', 2 ),
( 4, 'Mike', 3 ),
( 4, 'Mick', 4 ),
( 4, 'Michael', 1 ),
( 5, 'Will', 2 ),
( 5, 'Willie', 3 ),
( 6, 'Max', 4 );
```

This will result in a table of data that looks like this:

```
+---------+---------+---------+
| user_id | alias   | team_id |
+---------+---------+---------+
|       1 | Robert  |       1 |
|       1 | Bob     |       2 |
|       1 | Bobby   |       3 |
|       2 | Anna    |       1 |
|       2 | Ann     |       2 |
|       2 | Ann     |       3 |
|       2 | Ann     |       4 |
|       3 | Kathy   |       1 |
|       3 | Kate    |       2 |
|       4 | Mike    |       3 |
|       4 | Mick    |       4 |
|       4 | Michael |       1 |
|       5 | Will    |       2 |
|       5 | Willie  |       3 |
|       6 | Max     |       4 |
+---------+---------+---------+
```

Your task is to write a query that will result in a table that looks like the following:

```
+---------+-------------+------------+
| user_id | alias_count | team_count |
+---------+-------------+------------+
|       2 |           2 |          4 |
|       1 |           3 |          3 |
|       4 |           3 |          3 |
|       3 |           2 |          2 |
|       5 |           2 |          2 |
|       6 |           1 |          1 |
+---------+-------------+------------+
```

Here is a list of requirements:

- Each row in the resulting table should be a unique user id
- `alias_count` simply counts how many unique aliases a user has across teams
- `team_count` simply counts how many teams a user belongs to
- Resulting table is sorted by `team_count` from most to least
