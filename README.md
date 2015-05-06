# Source Code to Accompany _Essential Slick_.

To run the examples, you need to [install SBT](http://www.scala-sbt.org/release/tutorial/Setup.html).

There's a folder for each chapter, and each folder contains an SBT project.

Each file is either the example from the book, or the scaffolding for the exercises.


## Chapter 1 (Basics), 2 (Selecting Data) and  3 (Creating and Modifying Data)

These projects contain a single source file, _main.scala_. Use the SBT `run` or `~run` command.

For example:

```
$ cd chapter-01
$ $ ./sbt.sh
...
> run
...
[info] Running Example
Creating database table

Inserting test data

Selecting all messages:
Message(Dave,Hello, HAL. Do you read me, HAL?,1)
Message(HAL,Affirmative, Dave. I read you.,2)
Message(Dave,Open the pod bay doors, HAL.,3)
Message(HAL,I'm sorry, Dave. I'm afraid I can't do that.,4)

Selecting only messages from HAL:
Message(HAL,Affirmative, Dave. I read you.,2)
Message(HAL,I'm sorry, Dave. I'm afraid I can't do that.,4)
[success] Total time: 5 s, completed 06/05/2015 2:22:22 PM

```

## Chapter 4 (Data Modelling)

Chapter 4 contains several applications. Using the SBT `run` command will prompt you for the file to run.

Alternatively, use `runMain` or `~runMail` and supply the name of the class to run a particular example:

```
$ cd chapter-04
$ sbt
> ~runMain chapter04.StructureExample
```

The examples are:

1. `chapter03.StructureExample` in _structure.scala_ - an illustration of separating schema and profile.
2. `chapter03.HListExampleApp` in _hlists.scala_ - the HList example from the book.
3. `chapter03.NestedCaseClassExampleApp` in _nested_case_class.scala_ - is the exercise on custom case class mapping.
4. `chapter03.NullExample` in _nulls.scala_ - where the `User` table has an optional `email` field.
5. `chapter03.PKExample` in _primary_keys.scala_ - the `User.id` becomes an `Option[Long]`, and the `OccupantTable` is added.
6. `chapter03.ForeignKeyExample` in _foreign_keys.scala_ - where `MessageTable` has a foreign key to the `UserTable`.
7. `chapter03.ValueClassesExample` in _value_classes.scala_ - introduces types for primary keys, as `MessagePK` and `UserPk`.
8. `chapter03.SumTypesExample` in _sum_types.scala_ - the message `Flag`ing example from the book.
9. `chapter03.ModifiersExample` in _modifiers.scala_ -
10. `chapter03.CustomBooleanExample` in _custom_boolean.scala_ - is the "Custom Boolean" exercise code.

## Chapter 5 (Joins and Aggregates)

This project contains a _chat_schema.scala_ file that defines the schema for the chapter.
It also defines the method `populate` which inserts our standard cast, rooms, and messages into the database.

The schema is re-used in the following examples:

1. `chater04.JoinsExample` in _joins.scala_ - runs through a variety of joins using the sample data in _chat_schema.scala_.


## Chapter 6 (Plain SQL)

TODO: Add contents

