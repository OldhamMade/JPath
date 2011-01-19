JPath
=====

XPath for JSON
--------------

JPath is a simple lightweight Javascript Class which provides an XPath-like querying ability to JSON objects. This project extends the great work done by Bryan English at (bluelinecity.com)[http://bluelinecity.com].

Usage
-----

    var jpath = new JPath( myjsonobj );

    var somevalue = jpath.$('book/title').json;  //results in title
      //or
    var somevalue = jpath.query('book/title');   //results in title


Supported XPath Syntax:
-----------------------

From the original library:

    /tagname
    //tagname
    tagname
    * wildcard
    [] predicates
    operators ( >=, ==, <= )
    array selection
    ..             
    *
    and, or
    nodename[0]
    nodename[last()]
    nodename[position()]
    nodename[last()-1]
    nodename[somenode > 3]/node
    nodename[count() > 3]/node
    nodename[...][...]

Additional syntax:

**is null:** `nodename[is null]`
**is not null:** `nodename[is not null]`
**exists():** `nodename[exists(nodename)]`
**matches():** `nodename[matches(nodename, '^regex$')]`
**starts-with():** `nodename[starts-with(nodename, 'string')]`
**ends-with():** `nodename[ends-with(nodename, 'string')]`

Array-based queries:

**in:** `nodename[x in (1,2,"foo","bar")]`
**has:** `nodename[has "foo"]`
**empty:** `nodename[emptyarray is empty]`
**not empty:** `nodename[emptyarray is not empty]`

For more examples please see the unit tests.
