An H1 heading
=============

foo bar baz



An H2 heading
-------------

foo bar baz



### An H3 heading ###

foo bar baz



#### An H4 heading ####

foo bar baz

% Title
% Author Name
% 2012-04

The rest of the doc ...

*Italic*, **bold**, `code`.

    block of code
    goes like this

Or, as an alternative, delimited blocks are supported too:

~~~
block of code
goes like this
~~~

A syntax-highlighted code block:

~~~python
for i in range(10):
    print "hi", i
~~~


Please find [a link to the site](http://example.com/).

Also useful is [this site], as you may have heard.

[this site]: http://example2.com

Here comes an image:

![alt text](path/to/image.png)

Finally, don't miss <http://example3.com>.

Unordered list:

  * item 1
  * item 2
  * item 3

A longer one:

  * this is a long, multi-line paragraph. It
    seems to go on and on.

  * this is a long, multi-line paragraph. It
    seems to go on and on.

        Here's a code block
        within the list item.

    Here's a second paragraph, still part of
    the 2nd item.

  * this is a long, multi-line paragraph. It
    seems to go on and on.

Numbered:

 1. won
 2. too
 3. tree

Definition list:

foo
  : a foo-like object
bar
  : barium
baz
  : my third and final def list item

Done.

Here's a blockquote:

> He said *this*.
> I said *that*.

Done.

A table:

Size  Color   Fragrance
----  ------  ----------------
9     Red     Excelsior
10    Blue    Icey Cool
8     Green   Breezy Meadow

A multi-line table:

-------------------------------------------
Orientation  Reasoning
-----------  ------------------------------
leftward     Because it works well under
             extreme depths and pressures.

spinward     There's no reason to use
             spinward. It will only
             cause apoplexia.
-------------------------------------------

Done.

Here's a horizontal rule:

***

One minor footnote [^1] to be aware of.

[^1]: footnote text goes here.

You can simply <span class="yo">add html</span>,
if necessary. You can also escape to LaTeX-formatted
math: $a^2 = b^2 + c^2$.

<!-- This is a long comment,
     spanning multiple lines.
-->


Pandoc Markdown doesn't have these. You
might try for a similar effect like so:

| **Name**: Fluxor
| **Planet of origin**: Betatron 5
| **Special Skills**: Invisibility, Scent matching

or maybe put them into a table, or a definition list.
