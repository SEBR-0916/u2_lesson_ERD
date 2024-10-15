# Entity Relationship Diagrams (ERD)

![](https://www.conceptdraw.com/solution-park/icons/SD_TOOL_ERD/spbanner.png)

_"Failing to prepare is preparing to fail"_ - A truism for Server Side coding


## Overview

In this lesson, we'll talk about one of the most important aspects of building an **organized** and **efficient** database. ERD's are diagrams that allow us to plan what our database will look like and contain before we ever write a line of code.

## What Are ERD's?

ERD stands for Entity Relationship Diagram. It is a tool used to plan out a database by defining what tables/collections we'll have and how they associate to other tables/collections. There are special symbols that are used in order to model the direction of the relationship in a parent/child format (for the most part).

### Types Of Relationships

In the world of databases, there are many ways to relate data. We'll only use a few of them during this course. Here's a list of the types of relationships we'll use:

| Relationship | Description                                                                                                                                         | Example|
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------- |-------------------------------|
| One-To-One   | One parent can only have one child                                                                                                                  |A citizen has one Passport.    |
| One-To-Many  | One parent can have many children. A child can only have one parent. We use a foreign key/reference (typically a unique value such as the ObjectId) |A class has many Students.     |
| Many-To-Many | Many parents can have many children, join table/collection is used as a middleman to store both references                                          |Many airports have many flights|


### Relationship Symbols

In order to model a relationship, we need to use special symbols called `Crow's Feet` for this exact use. ERD's are an industry standard typically used by database admins/backend engineers.

For a full list of symbols, reference the following example:

![](https://i.stack.imgur.com/5uwcF.png)

It's important to note the direction in which you put the symbols is important! The direction dictates the type of relationship and how data relates to each other. For example if we wanted to use the previous tables to model `owners has-one homes` we could do the following:


Take note of the type of symbols we used and to what field they are pointing to:

- We point one end to the **owners** `_id` field and the other to the `owner_id` field in the **homes** table/collection

What if we wanted to model a `one-to-many` relationship?


- In this scenario, one person can have one or many pets
- We reflect that with the `one` symbol on the `persons` side of the diagram and the `one or many` symbol on the `pets` side of the diagram.

## Conventions

For the most part, the name of the collection/table is always **underscored** and **pluraled** while the fields are **singular**. This is a convention that comes from SQL/Relational based databases and is widely adopted accross the industry. If in doubt always consult your companies style guide and ask questions.

Key Value Pairs in our ERD should be the Property, and the Datatype associated. ~Not~ an example of the data, ie:

```
{
userName : string,
age : number
}

```

not

```
userName : "fakeUser123",
age: : 25
```


## Benefits Of An ERD

An ERD helps us have a concise plan/map of what our data should look like. It's one of the most important planning phases of any full stack project. Without an ERD you'll typically run into the following issues:

- Backpedaling to change your schemas, in MongoDB this means you'll have to destroy the entire database.
- Second guessing relationships / modeling relationships incorrectly.
- Overly complicated data structures that can be simplified or organized in a more efficient way.
- Sharing data and planning with team mates, managers, or investors/shareholders


## How Do You Draw An ERD

There's a few free and readily available tools that can be used to design and build ERD's. Below you'll find a list of those tools:

- [Lucid Chart](https://www.lucidchart.com/)
- [DrawIO](https://app.diagrams.net/)

The tools listed above are intuitive and simpler to use than others and are more than adequate to build ERD's during this course. They also have really awesome tutorials on how to do anything with them!

## You Do - 15 minutes

Designing a mock e-commerce site, create an ERD with 3 models, a User, a Shopping Cart, and Products. Create property key value pairs for each of these models and relate them using association you think would be most appropriate

## Recap

In this lesson, we learned about ERD's and the important roles they play in the software engineering world. You should always tackle any project with a clear direction and a well planned approach.
