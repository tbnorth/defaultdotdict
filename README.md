# DefaultDotDict

Yet another Python `dict` subclass that allows `my_dict.x` as
well as my_dict['x'].  The former is much more usable in equations
etc.

In addition, for non-existent keys it defaults to another
`DefaultDotDict`, so you can write:

```python
car = DefaultDotDict()
car.coord.x = 45.1235
car.coord.y = 92.5432
```

without having to define `car.coord`.

Other features:

 - `DefaultDotDict.json_load(open("somefile.json"))` will load JSON data
 using `DefaultDotDict`s (only for `dict`s within `dict`s, not `dict`s
 within `list`s).
 - `print(my_dict.key_tree())` shows a content listing of the
 `DefaultDotDict`.
