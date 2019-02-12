# Introducing Functions (Lesson 3)

Second class! In this lesson, we're going to continue our dive into variables,
providing a refresher of last class, while introducing how to use them in more
ways within our code.

Additionally, we'll introduce the usage of a code editor, which will allow us to
write more complex lines of code, save a file, and re-run it over and over
again.

It's important we continue to establish names so as we do attendance, we'll go
around asking names of each class member.

## Review: Variables

Before we move onto learning additional concepts, let's review variables. In
addition to a review, let's try using them in a few more interesting ways!

### Question: Do we remember how to declare a variable?

> Ask the class to guide the definition.

    first_name = "Bartek"
    last_name = "Ciszkowski"

Remember, variables can be anything that can vary. What else can we put in a
variable? Well, we can put numbers. Let's define the cost of some items

    apples = 2.5
    oranges = 3
    figs = 8

Numbers! This looks like a shopping list with prices now. Can we add them
together?

### Question: What if we add together first and last name? 

> Run the code, and point out the error (attempt to perform arithmetic on
> a string value)

And just because these are in variables, doesn't mean we can't do it without. We
can just add numbers in the terminal as normal. Variables help because it stores
a specific number in the computers memory for us, so we don't have to remember
what was in there.

But, back to variables. Like in arithmetic, BEDMAS is respected. Let's try it
with our receipt example by adding some taxes.

    apples = 2.5
    oranges = 3
    figs = 8
    + 13% taxes

Do you know the appropriate answer to this? Let's work it out as a clas (Should
be `15.3` rounded up from `15.255`)

### Activity

Take some time to practice this idea!

* Make your own shopping list of three items
* Store the cost of each item in a variable that labels the cost
* Work to add 13% taxes to the total cost of all your items, providing you the
    final total to pay.

Ensure everyone is able to get a proper subtotal before moving on.

### Introducing An Editor

So far, we've been writing code in the Lua shell. As we mentioned last week, the
shell is the little world we recreate each time we open Lua. We can, and will
also write code in fils that are saved on your computer and can be rerun
multiple times. An editor becomes useful as we go into writing more complex code
and we'll explore the benefits over the next few weeks.

Main things to go over in an editor review:

* Create a folder on your desktop for your Lua work. Call it `Lua`
* Open up Visual Studio Code and create a new file named `functions.lua` that'll
    be saved in that folder. We should go around and ensure that everyone has
    that.
* Ensure the `Terminal` can be opened up within VS Code so they can run the file
    and see the output in a single space.

This editor gives us one major benefit and I just mentioned it. It's a single
space to work on your program so you don't have to bounce between multiple
windows and applications. But more importantly, it allows us to write more than
one line of code in a way that is readable.

Tip: Use `Windows Key` + `+` to increase the font size if you find it too small!


### Introducing Functions

Now that we've introduced an editor, it's time to write more complex code! We'll
go into Visual Studio Code and make a new file, named `math.lua`

Then, let's write the following:

    function add(a, b)
        return a + b
    end

    total = add(1, 2)
    print(total)

Question time! Let's read this code from top to bottom to fully understand, but
we'll play with it to truly get how it works.

* We define a function and give it a name (`add`), and it takes two variables as
    parameters. Parameters is the name we give to variables that enter functions
* The function returns the result of `a` + `b`. If a functon returns nothing, it
    tells nothing back to the program, so it's important it does this.
* The function is ended when we wish. It's important we end a function, just
    like we will end other ideas in Lua
* We make a new variable which will hold the total of the `add` function, then
    we _call_ the function. To call a function means we run the code we made for
    it.
* Then we use `print` to show the total on the screen. If we don't print it, it
    won't show up, but it'll be in the program's world!

Go over line by line with the class, but reinforce that the best way to learn
this will be through practice and activities.

### Activity Time: Make your own subtract function!

We've made an `add` function, what about a `substract` function? Let's try to
apply the same ideas as we did for add, but in reverse. Then, we can play with
our two functions.


We've made an `add` function, what about a `substract` function? Let's try to
apply the same ideas as we did for add, but in reverse. Then, we can play with
our two functions.

* Create a new function named `subtract` in the same `math.lua` file
* Call the function and print the output with the parameters of your choice.

Now, let's play with it:

* Call your subtract function independently
* Call the add and subtract functions together into the same variable and print
    it out

Notice how we use the `+` sign to call multiple functions? If we translate this
to purely numbers, it's just arithmetic! For example:

    add(1, 2) + subtract(3, 5)

Translates into

    (1 + 2) + (3 - 5)

### Activity: Let's make a receipt calculator!

An important part of programming is being able to break down a problem into
small steps of logic. When you think about a calculator for a receipt, what
parts do you need to come to a solution?

We're going to keep this quite simple today, but can expand on it in the future
when we learn more programming concepts.

* Each line on a receipt will show a name and the total 
* We have a specific tax (13%) we want to add to the _subtotal_
* Our receipt should then show a total with taxes included.

For the first item, what do we need? Well, we need variables containing the cost
of each item, like we did before.

Let's make a new file named `receipt.lua` and begin defining three grocery items
of your choice again:

    apples = 3.5
    oranges = 2
    figs = 12

We'll want to add these up as a `subtotal`. We can use our add function, but
we're just adding numbers so we can add them directly into a new variable

    subtotal = apples + oranges + figs

Now, we need taxes. For this, let's make a new `multiply` function just to
practice!

    function multiply(a, b)
        return a * b
    end

Now, make a new variable that'll keep the taxes within it:

    taxes = multiply(subtotal, 0.13)

Finally, we can produce the total cost of the receipt:

    total = subtotal + taxes
    print(total)

As we dive further into functions we'll be able to use them in more complex
ways, that allow us to truly re-use code and build complex applications. This
exercise was focused on ensuring you practice writing them out and using them in
the simplest form.

### Extended Activity

If there is time, try making a receipt function which takes three variables as
parameters (the cost of three items), does the necessary calculations, and
returns a single number as the total.
