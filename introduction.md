# Introduction (Lesson 1)

First class! In this lesson, we're focused on setting the stage for the
semester, and hitting some preliminary goals

* Introduce names (teachers, mentors, students)
* Introducing Lua
* Discuss as a class the possibilities of what we can create
* Begin understanding the concepts of computational creation
* Begin establishing a culture of fearlessness, exploration, and peer collaboration

The notes are written as they would be told to the class, so that if the person
reading the lesson were a student, it'd be framed for them.

## Introducing names

It's important we establish a class room where we can use each others names and
promote the individual. As part of the introduction to this class, everyone will
go around and introduce themselves.

In addition to this, it's important the instructors ask individuals names early
and often to instill those within memory.

In addition, we'll want to separate the class into groups of three. These will
be chosen by the teacher(s) and group members will sit together.

The goal of each group will be to support each other throughout each week. There
are no individual or group marks, but we'll have some a fun quiz at the end of
the semester.

## Introducing Lua

Lua! What a lovely name. Going into this class, we want to define what we're
looking to get out of learnnng this language in particular.

And in fact, the primary reason for choosing Lua is because it will allow us to
learn a programming language without getting too much in our way.

What do I mean by getting in our way? Well, there are hundreds, if not thousands
of programming languages available for anyone to use. You'll see all sorts
of quirky things in programming like so:

    print("Hello World")

Notice the brackets and the double quotes around the word `Hello World`. Or, you
may get things like this:

    if (apple == orange) {
        println("Hello World");
    }

Where you see these curly braces, more brackets, and whoa, a semi-colon!

One of the first things we'll learn is why these extra characters are important
for a programming language and what they do.

Which gets us back to the first point -- not getting in our way.

We'll be using Lua because programming languages have many quirks. They mostly
need these quirks in order to translate to the computer what they _want_ to do,
but sometimes, it's because whoever designed them had certain ideas!

Lua is a programming language that reads a lot like English. For example:

    if apple == orange then
        print("Hello World")
    end

We still have to use a few special words, like telling Lua `Hey, "end" this
idea`, but Lua does this with style!

Which brings us to our first lesson. We humans, we're pretty smart. When your
friend asks you to make a peanut butter and jelly sandwich, you have a pretty
good idea of the steps involved.

Computers, well, they aren't necessarily dumb, but they rely on us humans for a
lot of instruction. So, when we tell a computer to make peanut butter and jelly
we have to be very specific! Let's take a look at an example again

**Group Activity Time!**

Now, before we dive into this example, we're going to run Lua on our computers.
Specifically, we're going to run something called the Lua interpreter. This is a
piece of Lua which allows us to write Lua code quickly without worrying about
saving files. It's a great way to test code, and most languages have this!

So, let's open up our Terminal (or Windows Command Prompt) and type the
following:

    lua

We should see something like so:

    21:57 $ lua
    Lua 5.3.5  Copyright (C) 1994-2018 Lua.org, PUC-Rio

Let's try typing something:

    > print("Hello World")
    Hello World

Here, we told Lua -- please print Hello World -- and of course, it did it.

Now let's try an example where we intentionally confuse Lua

    print("Hello

Press enter (you'll have to press it twice), and you should see this:

    >> stdin:1: unfinished string near '"Hello Worl'

What did I miss there? In the computers mind, it's still waiting for me to
finish the instruction. I never _closed_ the bracket, and likewise, did not
_close_ the word (what we call _strings_ in programming). Lua is actually
telling us in pretty plain English `unfinished string near...`, so that's pretty
cool.

Programming languages like Lua help us out here by telling us _Hey! You wrote
bad code!_ when we do things like this, which we call _errors_, but we need to
keep our eyes open, as it just makes our lives a bit easier. Let's fix that
code.

    print("Hello World")

Just like it was our first time! We will say this often in our class -- phrases like
_closing the bracket_, _closing the string_. The primary idea you'll want to
remember is anything that opens, must be closed. Brackets are always paired, as
are double quotes, etc.

We'll practice these concepts every week, and they will become normal very soon.

Before we move on, let's keep our Lua interpreter open and write some more code
to practice a few more ideas. Try this:

    print("enter a number")
    a = io.read("*number")
    print(a)

As you write this, Lua will ask you for a number -- because it's what you wrote
-- and then it'll print the number output, as stored in this letter `a`

That begins going into our next major concept, assignment, and we'll get to that
next, but what you saw here was the interaction you can have with a programming
language and an introduction to some of its quirks.

## What's Possible?

Programming is all around us. Every device, no matter how simple or complex is
programmed in some way. We understand not everyone wants to be a software
engineer, but being comfortable with computers and understanding how to
logically structure an application will open up other parts of your creative
brain and perhaps even let you apply programming concepts to other hobbies!

For example, many musicians, woodworkers, artists use programming to help their
craft, by either automating ideas, prototyping quick thoughts, or just being
another tool they can use whenever they need.

Programming is a creative form, and what we'll do in this class is focus on
embracing those creative aspects of programming while learning the fundamentals.

Because we want to keep it extra fun, we'll work on building interactive art and
a simple game using Lua. We'll do this with something called a _framework_, and
that framework is called [love2d](https://love2d.org/)

love2d can make professional games and of course, hobby games! We won't have a
ton of time to make the most complex game, but we will use our Lua learnings and
take advantage of love2d to take what we learn and make it a bit more visual.

In our next lesson, we'll begin to learn more fundamentals, focusing on this
idea of _assignment_ and _variables_. These concepts are another core part of
programming which must be understood in order for us to continue doing anything.
