Using the declare builtin restricts the scope of a variable
```
        foo ()
        {
        FOO="bar"
        }

        bar ()
        {
        foo
        echo $FOO
        }

        bar   # Prints bar.

```
A declare -f line with no arguments in a script causes a listing of all the functions previously defined in that script.

```
    declare -i #integer
    declare -r #readonly
    declare -a #array

```
`$RANDOM` returns a different random integer at each invocation.
    Nominal range: 0 - 32767 (signed 16-bit integer).

The only times a variable appears "naked" -- without the $ prefix -- is when declared or assigned, when unset, when exported, in an arithmetic expression within double parentheses (( ... )), or in the special case of a variable representing a signal 
Note that $variable is actually a simplified form of ${variable}.

Enclosing a referenced value in double quotes (" ... ") does not interfere with variable substitution. This is called partial quoting, sometimes referred to as "weak quoting." Using single quotes (' ... ') causes the variable name to be used literally, and no substitution will take place. This is full quoting, sometimes referred to as 'strong quoting.' 
If there is whitespace embedded within a variable,  then quotes are necessary.  Escaping the whitespace also works.
```mixed_bag=2\ ---\ Whateve```
An uninitialized variable has a `"null"` value -- no assigned value at all
`An uninitialized variable has no value, however it evaluates as **0** in an arithmetic operation.`
`:` null command [colon]. This is the shell equivalent of a "NOP" (no op, a do-nothing operation). It may be considered a synonym for the shell builtin true. The ":" command is itself a Bash builtin, and its exit status is true (0).
$*, $@ positional parameters.
