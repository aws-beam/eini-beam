Eini - An Erlang INI parser
===========================
This is just an INI parser. That's it. No state, no gen_servers, no ets tables,
just a parser that returns a map and does not convert strings into atoms.

You're probably looking for the original: https://github.com/erlcloud/eini

Example
-------

Input file:
```
  [title1]
  key = value
  key2 = value2
  [title2]
  key = value
```

Result form:
```
  #{ <<"title1">> => #{ <<"key">> => <<"value">>,
                        <<"key2">> => <<"value2">> },
     <<"title2">> => #{ <<"key">> => <<"value">> }
   }
```

History
-------
This is a fork to decruft the parser of things it doesn't need (supervision,
ETS, gen_server) and make it use maps and not convert to atoms. Use maps
for goodness' sake. It's 2018 people.

Copyright
---------
Copyright 2011 by Accense Technology, Inc.
Copyright 2018 by Mark R. Allen
