byte_size('?') # 4
byte_size('Hello World') # 11
from functools import reduce


def count_occurences(arr, val):
    return reduce(
        (lambda x, y: x + 1 if y == val and type(y) == type(val) else x + 0),
        arr)

def difference(a, b):
    b = set(b)
    return [item for item in a if item not in b]
