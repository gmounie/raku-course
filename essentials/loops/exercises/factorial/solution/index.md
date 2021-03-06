---
title: Solution of ‘Factorial’
---

{% include menu.html %}

A factorial of `N` is a product of integer numbers from 1 to and including `N`. E.g., factorial of 4 is 1 * 2 * 3 * 4 = 24.

## Code

```raku
my $n = 8;

my $f = 1;
$f *= $_ for 2..$n;

say $f;
```

🦋 Find the program in the file [factorial.raku](https://github.com/ash/raku-course/blob/master/exercises/loops/factorial.raku).

## Output

Run the program a few times and try different values of `$n`.

```console
$ raku exercises/loops/factorial.raku
40320
```

## Comments

This program uses the `*=` operator, which is a shortcut for multiplication with the assignment: `$x *= $y` is equivalent to `$x = $x * $y`.

You can use a ’full‘ loop instead of a postfix form:

```raku
my $n = 8;

my $f = 1;
for 2..$n -> $x {
    $f *= $x;
}

say $f;
```

## More on this subject

We will return to this task a number of times. In this part of the course, we will also solve this problem recursively.

In the second part of the course, we will learn about the so-called reduction operators, which make the solution trivial. Also, there will be a way to define a custom operator `!` so that you can write `$n!` to compute a factorial. Finally, there will be another chance to see an interesting solution when we’ll talk about the `where` clause.

{% include nav.html %}
