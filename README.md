<!-- Zero width character is used to put extra blank lines before and after code -->

<h3>
    
```python

class webDeveloper(type):
    def __new__(cls, name, bases, attrs):
        for attr in attrs:
            if not attr.startswith("_"):
                __annotations__[attr] = Tuple[str, ...]
        attrs["__annotations__"] = __annotations__
        new_cls = super().__new__(cls, name, bases, attrs)
        new_cls = dataclass(new_cls)
        return new_cls


class Stack(metaclass=WebDeveloper):
    languages   = ("JS")
    frontend    = ("HTML", “CSS”)
    ongoing     = ("Git", "Python")
    
​
```
</h3>

