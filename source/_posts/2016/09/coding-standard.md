---
title: Coding Standard
date: 2016-09-10 00:48:03
tags:
---

{% blockquote Don't know who said it %}
The working code is the most accurate document.
{% endblockquote %}

I think, as a developer, when working, here are 3 basic rules needs to follow:
1. Implement the requirement with no error;
2. Acceptable performance;
3. Readable code.

The 1st one, it's the very basic one. If code cannot work correctly, it's useless. For the 2nd one, it's a higher level request for the developer. When you coding, you should not only think how to write correct code, but also need to conside how to write high performance code, at least, not bad performance. To meet this rule, minimum, you should to know the common data structures, understand the algorithm complexity of the functions of those structures. And the last one, write readable code, it's the hardest part, and it's the most careless thing to developer. The code once has been written down, it doesn't mean it won't be changed any more. In the life cycle of the program, it could be 10 years or more, new requirements will be preposed continuously. That means the code needs to be changed. The creator may has left, someone new has to take over the job, or the creator has a long time not touch the code, he cannot remember every details. A terrible code will lead the job much more difficult. 

To define a coding standard is hard. Everyone has their preferences. Here I just want to list some very common things, and somethings I really recommend.

## Naming
It worths to spend some time to find out a name which can represent the exact meaning of the class, property, function or the variable. Don't use abbreviation unless you sure it is very common for every reader. And don't make the name too long, less than 30 characters should be fine. 
### Class Name
A class represents an object, so the name of if should be a noun, and use Pascal case for the capitalizing the name, like `AppDomain`.
### Properties
A property also represent an object, so the name also should be a noun, like `BackgroundColor`. It's also use Pascal case. If the property represents a collection, should use plural form of the noun, like `Items`.
### Functions
A function represent an activity, should use verb or the first word is verb, like `GetReader`. Or use `To` as the prefix, like `ToString`.
### Fields
Field is similar with the property, but for the protected instance filed should use Camel case, like `connectionString`. The `public`, `internal`, `static` fields should follow the Pascal case.
### Variables and Parameters
Variable or parameter also should be noun. But it should use Camel case. For the very simple functions, variables named as `x`, `a`, or other single character is acceptable. And for the very simple loop, `i` as the index variable name is acceptable too.
### Namespace
Namespace should use noun to name it too. And use Pascal case.
### Abbreviation
It's not recommended to use in classes, public properties, and public functions. Unless the name is too long, or the abbreviation is well known. If the name only have a word, it can (not must) use upper case for every charaters, like `ID`. If the name is composed of more than one words, for the abbreviation, only the first character can be upper case, like `XmlReader` or `HttpRequest`.
### Conventions
* Exception 
    Exception classes should use `Exception` as the suffix. For other cases, like `Reader`, `Event` also should add them as the suffix.
* Interface
    The name of the interface, should use `I` as the prefix.
* Try Functions
    Like `int.TryParse` function,  if you want to implement your own functions like this, please follow the same way, so that others can easy to know what it is and how to use it.

## Comments
* Add Xml document comment for public classes, properties, and functions. Give a short brief to describe what it is used for, what the input are expected, and what could be returned.
* Add Xml document comment for fields which name cannot explain the meaning or the usage.
* If you want to add some comments to explain something, describe why, not how.
* Don't add useless comments, like who or when changed the code.
* If the code is useless, delete it, don't comment it out.
* If the code changed, remember to update the comment.
* Keep in mind that the comments is obvious for now, but probably won't be obvious several weeks from now.  

## Formatting
### Tab VS. Space

### `this`

### Column Guideline

### Remove the empty multiple lines.

## Enum Type

## Switch

## Use Generic Types
