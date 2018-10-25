This file holds the tests that you create. Remember to import the python file(s)
you wish to test, along with any other modules you may need.
Run your tests with "python3 ok -t --suite SUITE_NAME --case CASE_NAME -v"
--------------------------------------------------------------------------------

Suite Uno

    >>> from scheme_reader import *

    Case Example
        >>> scheme_read(Buffer(tokenize_lines(['nil'])))
        nil

    Case Uno
    	>>> scheme_read(Buffer(tokenize_lines(['(* 3 2)'])))
    	Pair('*', Pair(3, Pair(2, nil)))

    Case Dos
    	>>> scheme_read(Buffer(tokenize_lines(['(- 5 (1 . 8) 4)'])))
    	Pair('-', Pair(5, Pair(Pair(1, 8), Pair(4, nil))))

