---
layout: post
title: "What is the difference between '===', '==', '.equal?' and
'.eql?' in Ruby?"
date: 2013-10-15 19:02
comments: true
tags: Ruby
summary: Coming from the PHP world, this was a little confusing. I deep dove into Ruby to discover how all this worked.
---

My years of programming have taking me along the lines of
learning Java in college, to PHP as a CMS hacker and now to Ruby. I was
recently going through an exercise in
[Exercism.io](http://www.exercism.io) and while somebody was
"nitpicking" my code, they mentioned that I probably didn't need the `===` in my
code. My code was making sure two variables were of the same type and
value. It looked a little like this:

``` ruby
# Bad - my original code
variableA === variableB

# Good - my new code
variableA == variableB
```

My nitpicker mentioned that I only needed `==`. But since I came from
the recent world of PHP, I was confused why I shouldn't use `===`. In
PHP, the double equals just checks for the same value and disregards
type. In Ruby, it's a whole different story.


I discovered it had to do with the fact that everything in Ruby is an
object and different objects can have different definitions for equality
(same goes for all object orient languages). Ruby's Object class has `===`, `.equal?`,
and `.eql?` by default. Many times Ruby classes override `==` but `.equal?` **should never be overriden**.

### What is the '=='?

At the Ruby Object level, `==` returns true only if the two compared
entities are the same object. Typically this is overriden in descendant
classes. You'll want to use this method if your object implements this. 

If you are looking for generic equality,
consider using, `.eql?`. You should look at your particular Ruby
object in question to see how they implemented `==`.

### What is the '==='?

#### `===` is the Case Equality Operator (Case Subsumption Operator)

The best answer I found was the Subsumption Operator answers the
question, "If I have a drawer labeled 'a' would it make sense to put 'b' in that drawer?"

```
(1..5) === 3           # => true
(1..5) === 6           # => false

Integer === 42          # => true
Integer === 'fourtytwo' # => false
```

### What is the '.eql?'
 
A good synonym phrase would be 'Generic Equality'. **The eql? method returns true if obj and other have the same value.**

The `.eql?` method returns `true` if both objects in question return the
same hash key. This is used by Hash to test members for equality. For objects of class Object,
`eql?` is synonymous with ==.

Subclasses normally continue this tradition, but there are exceptions. Numeric types, for example, perform type conversion across ==, but not across eql?, so:

```
1 == 1.0     #=> true
1.eql? 1.0   #=> false
```

The Ruby Documentation explains `==` well:

> At the Object level, `==` returns true only if obj and other are the same object.
> Typically, this method is overridden in descendant classes to provide class-specific
> meaning.

### What is the '.equal?' - determines object identitfy

This is effectively pointer comparison. "Is this the *exact* same
object?"

### tldr;

Equality in Ruby is confusing. You'll want to be informed when using it
and make sure you have an effective test suite.

`==` is overriden on a per class basis. Usually you'll
want to use the class's implementation of equals.

`===` answers the question "If I have a drawer labeled 'a', would it
make sense to put 'b' in that drawer?". You don't use this as often.

`.equal?` should never be overriden by a subclass.

```
a = "a"         # => "a"
other = a.dup   # => "a"

a == other      # => true
a === other     # => true
a.eql? other    # => true
a.equal? other  # => false
```

#### Resources

[Ruby Object Docs](http://ruby-doc.org/core-2.0.0/Object.html)

[Ruby String === Docs](http://ruby-doc.org/core-2.0.0/String.html#method-i-3D-3D-3D)

[Stack Overflow 1](http://stackoverflow.com/a/4467823/652200)

[Stack Overflow 2](http://stackoverflow.com/a/7157051/652200)
