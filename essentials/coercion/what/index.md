---
title: Introspection with `WHAT`
---

{% include menu.html %}

It is possible to see the type of data in a variable by calling the `WHAT` method on it:

```raku
my $n = 42;
my $s = '42';
say $n.WHAT; # (Int)
say $s.WHAT; # (Str)
```

The type is printed in parentheses, as shown in the comments. For example, `(Int)` or `(Str)`.

There is no problem to call a method on a literal itself. For example:

```raku
say 42.WHAT;      # (Int)
say (-1).WHAT;    # (Int)
say 'Hello'.WHAT; # (Str)
say True.WHAT;    # (Bool)
```

Notice that in the case of `-1`, we put the number in parentheses, as `say -1.WHAT` would try to negate the result of `1.WHAT`, which leads to an exception.

{% include nav.html %}
