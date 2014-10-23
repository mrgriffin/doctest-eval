doctest-eval
============

Fork of Python 2.7's doctest adding support for dict literals and other evalable expressions

Behaves like regular doctest except when the expected expression can be `eval`ed *and* the final statement in the REPL is an expression, in that case the result of that expression is compared with the `eval`ed expression using `==`.

This means that dicts, sets etc are suitable for use in a doctest, both the following pass:

    >>> {1, 2}
    {1, 2}
    
    >>> {1, 2}
    {2, 1}
