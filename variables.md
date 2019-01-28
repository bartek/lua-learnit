# Variables & Assignment (Lesson 2)

Now that we've loaded up Lua and are able to print out information, we want to
make it a bit more interactive and interesting!

One major component of any program is a variable. 

**Question**: Can anyone tell me what a variable is? Perhaps you learned in a
previous class?

Great! The simplest way to look at a variable is that it's a space in our
program to hold some set of information.

What that information is, how big or small it is, and where that space is used
can all vary. And to put it simply, what information can exist in a variable can
indeed, vary. A variable can vary [in information]. :)

## Our First Variable

Alright! Let's work together to assign and print out our first variable. We'll
continue to use our name for this exercise. First, I want you to open up Lua and
type just your first name with no spaces or double quotes, into Lua, like so:

    > Bartek
    nil

The result, as you can see is this word `nil`. `nil` in Lua speak means
"Nothing", or "None", or "Does Not Exist'. What Lua is saying here is that this
_variable_ that we are claiming as `Bartek` does not exist.

In programming, we must be very detailed. Back to our peanut butter and jelly
sandwich example, you, as a human who has grown up around food understands what
that sandwich is, and what are the parts of it.

But a computer, unless it's been told before and built by someone else, won't
know what `peanut butter` or `jelly` is.

Ok! Let's apply this concept to making a variable that'll store our name. Back
to Lua, everyone please do the following:

    > name = "Bartek" (Change to your name)

What we've done here is assigned the word `Bartek` to the new variable `name`.
Whenever we do this, we call it assignment. You'll notice we put double quotes
around our name. This is because we're telling Lua this is a string. A string
can be any collection of numbers or letters, and it must be wrapped in double
quotes.

We'll learn more about strings and other _types_ in a future lesson.

Now, when we made that assignment, nothing really happened. But we can now
output our assigned variable in Lua, let's try to assign and then output again.

    > name = "Bartek"
    > name
    Bartek

Aha! Lua now knows what `name` means. Remember, when we tried to output a
variable that did not exist, Lua told us `nil`. We can try that again:

    > name
    Bartek
    > last_name
    nil

`last_name` is another variable that we never defined, and Lua doesn't know what
it is. In its world, that's nothing, but because we can assign whatever we want
to any (sane) variable name, we can make that assignment in the future if we
need.

## Assignment In Multiple Variables

Let's continue practicing assignment. Our goal will be to make three variables.
One for our age, one for our first name, and one for our last name.

Let's open up Lua and define all three:

    > first_name = "Bartek"
    > last_name = "Ciszkowski"
    > age = 33

**Ask the Class**: What interesting things did you notice about how I defined my
variables?  (... Double quote usage and then not, the underscores in variable
names)

Now, we can of course output these into Lua as we've done before, and we see
this working well!

    > age = 33
    > age
    33
    etc ...

But we want to construct a proper sentence. We'll use our first `function` in
Lua now!

## Introducing print

You can think of a function as a tool in a utility belt, or perhaps a LEGO
block. Let's use the LEGO block analogy because LEGO is awesome.

Thus, a function can be imagined as a single piece of LEGO. That block of LEGO
is a particular colour, shape, size, and helps build your project in a certain
way. 

Most functions in programming do one thing, and do it well. In our example,
`print` does one thing: it prints text to the screen, and it does this pretty
well because as long as we respect how it wants to be implemented, it works!

We saw `print` earlier, but now we'll use it with variables, which is where the
power of it really shines. Here's a simple example using just my first name.

    > print("My name is " .. first_name .. ")
    My name is Bartek

We need to look at this function long and hard to see what's interesting about
it. What can we see? (Ask the class)

* We wrap the entire contents of the print function with parenthesis.
* We use double quotes a few times. If you look closely, you see they are used
    whenever a string begins or ends.
* We use this interesting pattern of two dots surrounding a variable name to
    insert the variable into the string.

On the last point, that is called _string interpolation_, but what really
matters is that we're able to use this technique to insert variables into the
print function.

We can do this with multiple variables, so let's do it with all the ones we
defined into a proper sentence.

    > print("My name is " .. first_name .. " " ..last_name .. and I am " .. age .. " years old")

Try typing that out! It'll be a little odd, but treat the dots (`..`) as
separators. Whenever you want to put a variable into a string, you use those
dots. You can see even when I want to add a space between first and last name, I
need to add a small string that is a space. Like we said, a string can be
any collection of letters and numbers, and of course in this case, spaces or
symbols.

## Wrapping Up

As a final exercise, try paying with the string above. Change the words, remove
the space between first and last name, tinker with the dots, and see what you
can find. We'll go around class to verify how things are going.





