## Match pattern

### Special characters

. ? + \* ^ $ \\  
( ) \[ \] { } |

Need to be escaped with a backslash (\\) to match the actual character

-   Any other character matches itself

.

Matches one of any character

(...)

Groups elements into a single element (also captures contents)

(?:...)

Groups elements into a single element (doesn’t captures contents)

(...|...|...)

Matches one of the alternatives

### Character classes

\[abc\]

Matches any character (same as (a|b|c))

\[^abc\]

Matches any other character

-   Only ^ - \\ \] need to be escaped inside a character class
-   May include simple ranges (eg, \[a-z123A-F\])

\\d

Matches digits (same as \[0-9\])

\\D

Matches non-digits (same as \[^0-9\])

\\w

Matches alphanumeric (same as \[a-zA-Z0-9\_\])

\\W

Matches non-alphanumeric (same as \[^a-zA-Z0-9\_\])

\\s

Matches whitespace (same as \[ \])\*

\\S

Matches non-whitespace (same as \[^ \])\*

\* In _RegexRenamer_ the only relevant whitespace character is the space character

### Anchors

-   Anchors match the position between characters, not the characters themselves

^

Matches the position at the beginning of the line

$

Matches the position at the end of the line

\\b

Matches the position between a \\w\\W or \\W\\w (word boundary)\*

\\B

Matches the position between a \\w\\w or \\W\\W (non-word boundary)

\* \\b also matches at the beginning and end of a line

### Quantifiers

-   Quantifiers are normally greedy (match as much as possible)
-   When followed by ? they become lazy (match as little as possible)

?

Match the previous element zero or one times (one if possible)

??

Match the previous element zero or one times (zero if possible)

+

Match the previous element one or more times (as many as possible)

+?

Match the previous element one or more times (as few as possible)

\*

Match the previous element zero or more times (as many as possible)

\*?

Match the previous element zero or more times (as few as possible)

{_n_}

Match the previous element exactly _n_ times

{_n_,}

Match the previous element at least _n_ times (as many as possible)

{_n_,}?

Match the previous element at least _n_ times (as few as possible)

{_n_,_m_}

Match the previous element between _n_ - _m_ times (as many as possible)

{_n_,_m_}?

Match the previous element between _n_ - _m_ times (as few as possible)

### Unnamed captures

(...)

Capture text matched between parentheses to an unnamed capture

\\_n_

Match the text in capture #_n_, captured earlier in the match pattern

-   The order of unnamed captures are defined by the order of the opening parentheses:  
    (_reg_)_ex_((_re_)(_name_)_r_) — #1 = _reg_, #2 = _renamer_, #3 = _re_, #4 = _name_
-   _n_ > 9 is only available if you have more than 9 captures

### Named captures

(?<_foo_\>...)

Capture text matched between parentheses to a capture named “_foo_”

\\<_foo_\>

Match the text in capture “_foo_”, captured earlier in the match pattern

### Lookaround

(?=...)

Positive lookahead (match the position before the specified regex)

(?!...)

Negative lookahead (don’t match, as above)

(?<=...)

Positive lookbehind (match the position after the specified regex)

(?<!...)

Negative lookbehind (don't match, as above)

### Alternation

(?(_test_)_true_)

If positive lookahead _test_ matches, match _true_ regex

(?(_test_)_true_|_false_)

As above, otherwise match _false_ regex

(?(_capture_)_true_)

If _capture_ (name or number) contains text, match _true_ regex

(?(_capture_)_true_|_false_)

As above, otherwise match _false_ regex

### Inline modifiers

(?_x_)

Turn on modifier _x_ until the end of the containing group

(?-_x_)

Turn off modifier _x_ until the end of the containing group

(?_x_:...)

Turn on modifier _x_ for the section

(?-_x_:...)

Turn off modifier _x_ for the section

-   Relevent [modifiers](http://regexrenamer.sourceforge.net/help/regex_modifiers.html) are i (ignore case) and x (extended regex).
-   You may group more than one modifier together

## Replace pattern

Any text other than the variables below will be replaced as-is.

### Special variables

$_n_

Insert the contents of unnamed capture #_n_

${_foo_}

Insert the contents of named capture “_foo_”

$0

Insert all text matched in the regex (automatic unnamed capture)

$\` (backtick)

Insert text before $0

$' (single-quote)

Insert text after $0

$\_

Insert the entire original filename (same as $\`$0$')

$#

Insert a number sequence (see [Numbering](http://regexrenamer.sourceforge.net/help/interface_menus.html#Numbering))

$$

Insert an actual $ character (therefore, $$# to insert actual $#)

-   For unnamed captures, use ${_n_} if the following character is an actual digit
-   _n_ > 9 is only available if you have more than 9 captures

[![](http://sflogo.sourceforge.net/sflogo.php?group_id=177064&type=8)](http://sourceforge.net/projects/regexrenamer)