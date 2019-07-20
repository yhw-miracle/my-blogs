---
title: python基础
date: 2019-04-18 11:10:44
tags: []
categories: 知识总结
---
### `python`介绍
1. 解释型编程语言
2. `python`单行注释`#`
3. `python`多行注释`"""`与`"""`
4. `# TODO`说明文字

### 变量、关键字
1. 变量用于描述计算机中的数据存储空间，作用是在计算机内存中保存数据。
2. 变量名的命名规则是由数字、字母和下划线组成，不能以数字开头，不能是关键字，区分大小写。
3. 下划线连接，驼峰命名法
4. 关键字
```python
import keyword
print(keyword.kwlist)
```
![](/images/2019/Apr/01.png)

### 数据结构
#### 基本数据结构
1. 数值型：`int`、`float`、`bool`
2. 非数值型：`str`
3. `type()`：获取数据类型

| 名称 |含义 |
| ------ | ------ |
| int | 整型 |
| float | 浮点型 |
| bool | 布尔型 |
| str | 字符串 |

#### 列表
1. 列表（`list`）（`[]`）是一种存储大量数据的存储模型，可以对数据进行增、删、改、查操作。
2. 增加数据
| function | meanings |
| ------ | ------ |
| append(self, object) | Append object to the end of the list. |
| insert(self, index, object) | Insert object before index. |
| extend(self, iterable) | Extend list by appending elements from the iterable. |
 * 翻译：
(1). append(self, object): 在列表的末尾添加元素。
(2). insert(self, index, object): 在指定位置之前插入元素。
(3). extend(self, iterable): 从可迭代数据存储器中扩充到列表末尾。

3. 删除数据
| function | meanings |
| ------ | ------ |
| remove(self, object) | Remove first occurrence of value.Raises ValueError if the value is not present. |
| pop(self, index) | Remove and return item at index (default last).Raises IndexError if list is empty or index is out of range. |
| clear(self) | Remove all items from list. |
 * 翻译：
(1). remove(self, object): 移除列表中第一个指定数据，若指定数据不存在，抛出`ValueError`。
(2). pop(self, index): 移除并返回列表中指定位置的数据（默认为最后一个），若列表为空或者指定位置超过范围，抛出`IndexError`。
(3). clear(self): 移除列表中所有元素。

4. 修改数据和查询数据
 - 根据索引

5. 其他函数
| function | meanings |
| ------ | ------ |
| count(self, object) | Return number of occurrences of value. |
| index(self, object, start, stop) | Return first index of value.Raises ValueError if the value is not present. |
| copy(self) | Return a shallow copy of the list. |
| reverse(self) | Reverse *IN PLACE*. |
| sort(self, key, reverse) | Stable sort *IN PLACE*. |
 * 翻译
(1). count(self, object): 返回指定数据在列表中的个数。
(2). index(self, object, start, stop): 返回指定数据在列表中第一个位置，若指定数据不存在，抛出`ValueError`。
(3). copy(self): 返回一个列表的拷贝。
(4). reverse(self): 在列表上反转。
(4). sort(self, key, reverse): 在列表上执行稳定排序。

#### 元组
1. 元组（`tuple`）（`()`）是一种存储固定数据的存储模型，元组中的数据通过`索引`修改。
2. 元组中的数据若是`非引用类型数据`，不允许修改；若是`引用类型数据`，不允许修改对象，可以修对象的值。
3. 元组函数
| function | meanings |
| ------ | ------ |
| count(self, x) | Return number of occurrences of value. |
| index(self, x, start, end) | Return first index of value.Raises ValueError if the value is not present. |
 * 翻译
(1). count(self, x): 返回元组中指定数据出现的次数。
(2). index(self, x, start, end): 返回指定数据在元组中出现的第一个位置，若指定数据不存在，抛出`ValueError`。

#### 集合
1. 集合（`set`）（`{,,...}`）是一种存储无序不重复数据的存储模型，没有`索引`概念。
2. 集合中的函数
(1). add(self, element): Add an element to a set.This has no effect if the element is already present.
(2). clear(self): Remove all elements from this set.
(3). copy(self): Return a shallow copy of a set.
(4). difference(self, s): Return the difference of two or more sets as a new set.(i.e. all elements that are in this set but not the others.)
(5). difference_update(self,  s): Remove all elements of another set from this set.
(6). discard(self, element): Remove an element from a set if it is a member.If the element is not a member, do nothing.
(7). intersection(self, s): Return the intersection of two sets as a new set.(i.e. all elements that are in both sets.)
(8). intersection_update(self,  s): Update a set with the intersection of itself and another.
(9). isdisjoint(self, s): Return True if two sets have a null intersection.
(10). issubset(self ,s): Report whether another set contains this set.
(11). issuperset(self, s): Report whether this set contains another set.
(12). pop(self): Remove and return an arbitrary set element.Raises KeyError if the set is empty.
(13). remove(self ,element): Remove an element from a set; it must be a member.If the element is not a member, raise a KeyError.
(14). symmetric_difference(self,  s): Return the symmetric difference of two sets as a new set.(i.e. all elements that are in exactly one of the sets.)
(15). symmetric_difference_update(self,  s): Update a set with the symmetric difference of itself and another.
(16). union(self, s): Return the union of sets as a new set.(i.e. all elements that are in either set.)
(17). update(self,  s): Update a set with the union of itself and others.

 * 翻译
(1). add(self, element): 添加一个元素到集合中，若改元素已经存在，集合将无任何影响。
(2). clear(self): 移除集合中所有元素。
(3). copy(self): 返回集合的拷贝体。
(4). difference(self, s): 记录该集合与其他集合之间的不同元素，组成新的集合并返回（简单来说，返回集合中的所有元素在该集合中，不在其他集合中）。
(5). difference_update(self,  s): 移除另一个集合中与该集合相同的元素。
(6). discard(self, element): 移除集合中的指定元素，若该元素不存，则不任何事。
(7).intersection(self, s): 记录两个集合的交集，组成新的集合并返回（简单来说，新的集合中元素是两个集合中都有的元素）。
(8). intersection_update(self,  s): 将该集合和另一个集合的交集更新到该集合中。
(9). isdisjoint(self, s): 若两个集合没有交集，返回`True`。
(10). issubset(self ,s): 报告另一个集合是否包含该集合，若包含，返回`True`；若不包含，返回`False`。
(11). issuperset(self, s): 报告这个集合是否包含另一个集合，若包含，返回`True`；若不包含，返回`False`。
(12). pop(self): 移除并返回这个该集合中随意一个元素，若集合为空，抛出`KeyError`。
(13). remove(self ,element): 移除集合中指定的元素，若指定元素不存在，抛出`KeyError`。
(14). symmetric_difference(self,  s): 记录两个集合的均匀区别，组成新的集合并返回（简单来说，新的集合中元素只存在于其中一个集合中）。
(15). symmetric_difference_update(self,  s): 将两个集合的均匀区别更新到该集合中。
(16). union(self, s): 记录两个集合之间的并集，组成新的集合并返回（简单来说，两个集合中所有元素）。
(17). update(self,  s): 将两个集合之间的并集更新到该集合中。

#### 字典
1. 字典（dict）（{xx: xx,...}）是一种使用“键值对结构”存储数据的存储模型，没有`索引`概念，利用`键`（键是**唯一**的）来索引，可以根据`键`对字典数据进行增、删、改、查操作。
2. 字典中的函数
(1). clear(self):  D.clear() -> None.  Remove all items from D.
(2). copy(self): D.copy() -> a shallow copy of D.
(3). fromkeys(seq): Create a new dictionary with keys from iterable and values set to value.
(4). get(self, k): Return the value for key if key is in the dictionary, else default.
(5). items(self): D.items() -> a set-like object providing a view on D's items.
(6). keys(self): D.keys() -> a set-like object providing a view on D's keys.
(7). values(self): D.values() -> an object providing a view on D's values.
(8). pop(self,  k): D.pop(k[,d]) -> v, remove specified key and return the corresponding value.If key is not found, d is returned if given, otherwise KeyError is raised.
(9). popitem(self): D.popitem() -> (k, v), remove and return some (key, value) pair as a 2-tuple; but raise KeyError if D is empty.
(10). setdefault(self, k,  default): Insert key with a value of default if key is not in the dictionary.Return the value for key if key is in the dictionary, else default.
(11). update(self, E=None, \*\*F): D.update([E, ]\*\*F) -> None.  Update D from dict/iterable E and F. If E is present and has a .keys() method, then does:  for k in E: D[k] = E[k]. If E is present and lacks a .keys() method, then does:  for k, v in E: D[k] = v. In either case, this is followed by: for k in F:  D[k] = F[k].

 * 翻译
(1). clear(self): 清空字典中的所有项。
(2). copy(self): 返回字典的一个拷贝。
(3). fromkeys(seq): 用来自迭代器作为键，值集合作为值，创建新的字典。
(4). get(self, k): 返回指定的键对应的值。
(5). items(self): 获取字典中所有键值对，以列表形式返回。
(6). keys(self): 获取字典中所有键，以列表的形式返回。
(7). values(self): 获取字典中所有值，以列表的形式返回。
(8). pop(self,  k[, d]): 移除字典中指定的键，并返回对应的值。如果指定的键不存在，若给出`d`，则返回`d`；否则将抛出`KeyError`。
(9). popitem(self): 移除字典中最后一对键值对，并以二元元组的形式返回。若字典为空，抛出`KeyError`。
(10).setdefault(self, k,  default): 如果指定的键不在字典中，将指定的键和值（没有，默认为`None`）插入到字典中，并返回值。
(11). update(self, E=None, \*\*F): 使用新字典中的数据对原始字典数据进行更新。如果字典`E`存在，有`keys()`方法，则执行代码`for k in E: D[k] = E[K]`；如果迭代器`E`存在，缺失`keys()`方法，则执行代码`for k, v in E: D[k] = v`；如果字典或迭代器`E`不存在，则执行代码`for k in F: D[k] = F[k]`。

3. 当需要存储大量数据，并且期望在编程期以最快速度获取单个数据，或者使用非对象格式保存单个对象的属性值，推荐选择字典来存储。

#### 类型转换
```python
int()
float()
bool()
str()
tuple()
list()
set()
dict()
```
1. int()，字符串转换为整型数据。
2. float()，字符串，整型数据转换为浮点型数据。 
3. bool()，`bool`(0)为False，`bool(1)`为True。
4. list(tuple | set)
5. tuple(list |set)
6. set(list | tuple)

#### 公共方法
1. 元组、列表、集合、字典拥有的公共方法：`len()`、`max()`、`min()`。
2. 元组、列表和字符串可以进行`切片`获取局部数据，格式如下：`contain[start:end:step]`。

#### 字符串
1. 字符串是一个包含若干个字符并按照一定顺序排列成整体的容器，支持`索引`操作，字符串定义可以是`"xxxx"`,`'xxx'`,`"""xxx"""`,`'''xxx'''`。
2. 字符串的一些函数
isalnum(self, *args, \*\*kwargs): Return True if the string is an alpha-numeric string, False otherwise. A string is alpha-numeric if all characters in the string are alpha-numeric and there is at least one character in the string.

isalpha(self, *args, \*\*kwargs): Return True if the string is an alphabetic string, False otherwise. A string is alphabetic if all characters in the string are alphabetic and there is at least one character in the string.

isascii(self, *args, \*\*kwargs): Return True if all characters in the string are ASCII, False otherwise. ASCII characters have code points in the range U+0000-U+007F. Empty string is ASCII too.

isdecimal(self, *args, \*\*kwargs): Return True if the string is a decimal string, False otherwise. A string is a decimal string if all characters in the string are decimal and there is at least one character in the string.

isdigit(self, *args, \*\*kwargs): Return True if the string is a digit string, False otherwise. A string is a digit string if all characters in the string are digits and there is at least one character in the string.

isidentifier(self, *args, \*\*kwargs): Return True if the string is a valid Python identifier, False otherwise. Use keyword.iskeyword() to test for reserved identifiers such as "def" and "class".

islower(self, *args, \*\*kwargs): Return True if the string is a lowercase string, False otherwise. A string is lowercase if all cased characters in the string are lowercase and there is at least one cased character in the string.

isnumeric(self, *args, \*\*kwargs): Return True if the string is a numeric string, False otherwise. A string is numeric if all characters in the string are numeric and there is at least one character in the string.

isprintable(self, *args, \*\*kwargs): Return True if the string is printable, False otherwise. A string is printable if all of its characters are considered printable in repr() or if it is empty.

isspace(self, *args, \*\*kwargs): Return True if the string is a whitespace string, False otherwise. A string is whitespace if all characters in the string are whitespace and there is at least one character in the string.

istitle(self, *args, \*\*kwargs): Return True if the string is a title-cased string, False otherwise. In a title-cased string, upper- and title-case characters may only follow uncased characters and lowercase characters only cased ones.

isupper(self, *args, \*\*kwargs): Return True if the string is an uppercase string, False otherwise. A string is uppercase if all cased characters in the string are uppercase and there is at least one cased character in the string.

strip(self, *args, \*\*kwargs): Return a copy of the string with leading and trailing whitespace remove. If chars is given and not None, remove characters in chars instead.

lstrip(self, *args, \*\*kwargs): Return a copy of the string with leading whitespace removed. If chars is given and not None, remove characters in chars instead.

rstrip(self, *args, \*\*kwargs): Return a copy of the string with trailing whitespace removed. If chars is given and not None, remove characters in chars instead.

ljust(self, *args, \*\*kwargs): Return a left-justified string of length width. Padding is done using the specified fill character (default is a space).

rjust(self, *args, \*\*kwargs): Return a right-justified string of length width. Padding is done using the specified fill character (default is a space).

find(self, sub, start=None, end=None): S.find(sub[, start[, end]]) -> int   Return the lowest index in S where substring sub is found, such that sub is contained within S[start:end].  Optional arguments start and end are interpreted as in slice notation. Return -1 on failure.

rfind(self, sub, start=None, end=None): S.rfind(sub[, start[, end]]) -> int   Return the highest index in S where substring sub is found, such that sub is contained within S[start:end].  Optional arguments start and end are interpreted as in slice notation. Return -1 on failure.

index(self, sub, start=None, end=None): S.index(sub[, start[, end]]) -> int   Return the lowest index in S where substring sub is found, such that sub is contained within S[start:end].  Optional arguments start and end are interpreted as in slice notation. Raises ValueError when the substring is not found.

rindex(self, sub, start=None, end=None): S.rindex(sub[, start[, end]]) -> int   Return the highest index in S where substring sub is found, such that sub is contained within S[start:end].  Optional arguments start and end are interpreted as in slice notation. Raises ValueError when the substring is not found.

replace(self, *args, \*\*kwargs): Return a copy with all occurrences of substring old replaced by new. count: Maximum number of occurrences to replace. -1 (the default value) means replace all occurrences. If the optional argument count is given, only the first count occurrences are replaced.

partition(self, *args, \*\*kwargs): Partition the string into three parts using the given separator. This will search for the separator in the string.  If the separator is found, returns a 3-tuple containing the part before the separator, the separator itself, and the part after it. If the separator is not found, returns a 3-tuple containing the original string and two empty strings.

rpartition(self, *args, \*\*kwargs): Partition the string into three parts using the given separator. This will search for the separator in the string, starting at the end. If the separator is found, returns a 3-tuple containing the part before the separator, the separator itself, and the part after it. If the separator is not found, returns a 3-tuple containing two empty strings and the original string.

split(self, *args, \*\*kwargs): Return a list of the words in the string, using sep as the delimiter string. sep: The delimiter according which to split the string. None (the default value) means split according to any whitespace, and discard empty strings from the result. maxsplit: Maximum number of splits to do. -1 (the default value) means no limit.

rsplit(self, *args, \*\*kwargs): Return a list of the words in the string, using sep as the delimiter string. sep: The delimiter according which to split the string. None (the default value) means split according to any whitespace, and discard empty strings from the result. maxsplit: Maximum number of splits to do. -1 (the default value) means no limit. Splits are done starting at the end of the string and working to the front.

splitlines(self, *args, \*\*kwargs): Return a list of the lines in the string, breaking at line boundaries. Line breaks are not included in the resulting list unless keepends is given and true.

startswith(self, prefix, start=None, end=None): S.startswith(prefix[, start[, end]]) -> bool   Return True if S starts with the specified prefix, False otherwise. With optional start, test S beginning at that position. With optional end, stop comparing S at that position. prefix can also be a tuple of strings to try.

endswith(self, suffix, start=None, end=None): S.endswith(suffix[, start[, end]]) -> bool   Return True if S ends with the specified suffix, False otherwise. With optional start, test S beginning at that position. With optional end, stop comparing S at that position. suffix can also be a tuple of strings to try.

format(self, *args, \*\*kwargs): S.format(*args, \*\*kwargs) -> str   Return a formatted version of S, using substitutions from args and kwargs. The substitutions are identified by braces ('{' and '}').

format_map(self, mapping): S.format_map(mapping) -> str   Return a formatted version of S, using substitutions from mapping. The substitutions are identified by braces ('{' and '}').

lower(self, *args, \*\*kwargs): Return a copy of the string converted to lowercase.

upper(self, *args, \*\*kwargs): Return a copy of the string converted to uppercase.

swapcase(self, *args, \*\*kwargs): Convert uppercase characters to lowercase and lowercase characters to uppercase. 

title(self, *args, \*\*kwargs): Return a version of the string where each word is titlecased. More specifically, words start with uppercased characters and all remaining cased characters have lower case.

capitalize(self, *args, 、\*\*kwargs): Return a capitalized version of the string. More specifically, make the first character have upper case and the rest lower case.

casefold(self, *args, \*\*kwargs): Return a version of the string suitable for caseless comparisons.

center(self, *args, \*\*kwargs): Return a centered string of length width. Padding is done using the specified fill character (default is a space).

expandtabs(self, *args, \*\*kwargs): Return a copy where all tab characters are expanded using spaces. If tabsize is not given, a tab size of 8 characters is assumed.

zfill(self, *args, \*\*kwargs): Pad a numeric string with zeros on the left, to fill a field of the given width.The string is never truncated.


count(self, sub, start=None, end=None): S.count(sub[, start[, end]]) -> int   Return the number of non-overlapping occurrences of substring sub in string S[start:end].  Optional arguments start and end are interpreted as in slice notation.

encode(self, *args, \*\*kwargs): Encode the string using the codec registered for encoding.   encoding: The encoding in which to encode the string.   errors: The error handling scheme to use for encoding errors. The default is 'strict' meaning that encoding errors raise a UnicodeEncodeError.  Other possible values are 'ignore', 'replace' and 'xmlcharrefreplace' as well as any other name registered with codecs.register_error that can handle UnicodeEncodeErrors.

join(self, ab=None, pq=None, rs=None): Concatenate any number of strings. The string whose method is called is inserted in between each given string. The result is returned as a new string. `Example: '.'.join(['ab', 'pq', 'rs']) -> 'ab.pq.rs'`

maketrans(self, *args, \*\*kwargs): Return a translation table usable for str.translate(). If there is only one argument, it must be a dictionary mapping Unicode ordinals (integers) or characters to Unicode ordinals, strings or None. Character keys will be then converted to ordinals. If there are two arguments, they must be strings of equal length, and in the resulting dictionary, each character in x will be mapped to the character at the same position in y. If there is a third argument, it must be a string, whose characters will be mapped to None in the result.

translate(self, *args, \*\*kwargs): Replace each character in the string using the given translation table.table: Translation table, which must be a mapping of Unicode ordinals to Unicode ordinals, strings, or None. The table must implement lookup/indexing via \_\_getitem\_\_, for instance a dictionary or list.  If this operation raises LookupError, the character is left untouched.  Characters mapped to None are deleted.

 * 翻译
 * 判断函数
isalnum(self, *args, \*\*kwargs): 判断字符串是否字母数字。
isalpha(self, *args, \*\*kwargs): 判断字符串是否全是字母。
isascii(self, *args, \*\*kwargs): 判断字符串是否全是`ASCII`字符。
isdecimal(self, *args, \*\*kwargs): 判断字符串是否全是数字。
isdigit(self, *args, \*\*kwargs): 判断字符串是否全是数字。
isidentifier(self, *args, \*\*kwargs): 判断字符串是否是有效的`python`标识符。
islower(self, *args, \*\*kwargs): 判断字符串是否全是小写。
isnumeric(self, *args, \*\*kwargs): 判断字符串是否全是数字。
isprintable(self, *args, \*\*kwargs): 判断字符串是否是可打印的。
isspace(self, *args, \*\*kwargs): 判断字符串是否是空白字符。
istitle(self, *args, \*\*kwargs): 判断字符串是否是首字母大写，其他小写。
isupper(self, *args, \*\*kwargs): 判断字符串是否全是大写。

 * 格式转换函数
strip(self, *args, \*\*kwargs): 返回去掉字符串左右两侧空白字符或指定字符的拷贝。
lstrip(self, *args, \*\*kwargs): 返回去掉字符串左侧空白字符或指定字符的拷贝。
rstrip(self, *args, \*\*kwargs): 返回去掉字符串右侧空白字符或指定字符的拷贝。

ljust(self, *args, \*\*kwargs): 返回右侧用空格或指定字符补齐指定宽度的字符串。
rjust(self, *args, \*\*kwargs): 返回左侧用空格或指定字符补齐指定宽度的字符串。

center(self, *args, \*\*kwargs): 填充字符串左右两侧几乎相等的指定字符或空格，是字符串居于中间位置，返回这样的字符串。

zfill(self, *args, \*\*kwargs): 用`0`在数字字符串的左边补齐给定的宽度，字符串不会`truncated`。

 * 查询函数
find(self, sub, start=None, end=None): 返回指定字符串在原字符串中出现的最小下标。若给定`start`和`end`，则在指定范围里搜索；若指定字符串未发现，则返回`-1`。
rfind(self, sub, start=None, end=None): 返回指定字符串在原字符串中出现的最大下标。若给定`start`和`end`，则在指定范围里搜索；若指定字符串未发现，则返回`-1`。
index(self, sub, start=None, end=None): 返回指定字符串在原字符串中出现的最小下标。若给定`start`和`end`，则在指定范围里搜索；若指定字符串未发现，则抛出`ValueError`。
rindex(self, sub, start=None, end=None): 返回指定字符串在原字符串中出现的最大下标。若给定`start`和`end`，则在指定范围里搜索；若指定字符串未发现，则抛出`ValueError`。

 * 划分函数
partition(self, *args, \*\*kwargs): 从字符串左侧开始，根据指定参数将字符串划分为三部分，参数左侧、参数和参数右侧，组成三元元组并返回。如果指定参数不存在，三元元组由两个空项和自身组成。
rpartition(self, *args, \*\*kwargs): 从字符串右侧开始，根据指定参数将字符串划分为三部分，参数左侧、参数和参数右侧，组成三元元组并返回。如果指定参数不存在，三元元组由两个空项和自身组成。

split(self, *args, \*\*kwargs): 用指定参数作为分隔符将原字符串划分为若干字符串，组成列表返回。
rsplit(self, *args, \*\*kwargs): 用指定参数作为分隔符将原字符串从右侧开始划分为若干字符串，组成列表返回。
splitlines(self, *args, \*\*kwargs): 用分行符作为分隔符将原字符串划分若干个字符串，组成列表返回，其中分行符不会包括在结果字符串中。

 * 替换函数
replace(self, *args, \*\*kwargs): 使用新字符串替换原字符串中指定的字符串。

expandtabs(self, *args, \*\*kwargs): 返回用空格替换字符串中的制表位的拷贝。

 * 字符转换函数
lower(self, *args, \*\*kwargs): 返回字符串中各字符转换为小写字符的拷贝。
upper(self, *args, \*\*kwargs): 返回字符串中各个字符转换为大写的拷贝。
swapcase(self, *args, \*\*kwargs): 将字符串的大写字符转换为小写字符，小写字符转换为大写字符。
title(self, *args, \*\*kwargs): 返回首字母大写，其他小写的字符串。
capitalize(self, *args, 、\*\*kwargs): 返回字符串首字母大写，其他小写。
casefold(self, *args, \*\*kwargs): 返回字符串中所有字母转换为小写字母。

startswith(self, prefix, start=None, end=None): 如果字符串以给定字符参数`prefix`开头，返回`True`；否则，返回`False`。如果给定`start`和`end`参数，则从`start`和`end`的位置进行检测。
endswith(self, suffix, start=None, end=None): 如果字符串以给定字符参数`suffix`结尾，返回`True`；否则，返回`False`。如果给定`start`和`end`参数，则从`start`和`end`的位置进行检测。

 * 其他函数
format(self, *args, \*\*kwargs): 使用元组数据格式化字符串。
format_map(self, mapping): 使用字典类型数据格式化字符串。

count(self, sub, start=None, end=None): 返回指定的字符串在原字符串中出现的次数。如果给定`start`和`end`参数，则从`start`和`end`的位置进行检测。

encode(self, *args, \*\*kwargs): 使用指定的编码方式给字符串编码。

join(self, ab=None, pq=None, rs=None): 连接字符串，返回新的字符串。

maketrans(self, *args, \*\*kwargs): 返回函数`tranlate()`需要的翻译表。一般是`maketrans(str1, str2)`。
translate(self, *args, \*\*kwargs): 用给定的翻译表替换字符串中的每一个字符。一般是`translate(dict)`。

### 标准输入输出
#### 输入
1. input()
#### 输出
1. print()
2. %s，字符串占位符
3. %d，整数占位符
4. %f，浮点数占位符
5. %%，输入`%`

### python运算
#### 字符串运算
1. `+`：拼接
2. `*`：连续拼接

#### 算术运算符
1. `+`，加
2. `-`，减
3. `*`，乘
4. `/`，除
5. `//`，整除
6. `%`，取余
7. `**`，乘方
8. 优先级，乘方 > [乘，除，整除，取余] > [加，减]

#### 赋值运算符
1. =，赋值
2. +=，加后赋值
3. -=，减后赋值
4. *=，乘后赋值
5. /=，除后赋值
6. //=，整除后赋值
7. %=，取余后赋值
8. **=，次方后赋值

#### 比较运算符
1. \>，大于
2. \>=，大于等于
3. <，小于
4. <=，小于等于
5. !=，不低于
6. ==，等于
7. 查看字母和数字的`ASCII`值
查看`ASCII`值：ord()
已知`ASCII`值查看对应的字符：chr()

#### 关系运算符（逻辑运算符）
1. and
短路与，左操作数为`False`，表达式结果为`False`，与`左`操作数`bool`值相同。 
2. or
短路或，左操作数为`True`，表达式结果为`True`，与`左`操作数`bool`值相同。
3. not
4. 一些例子
| 表达式 | 结果 |
| ------ | ------ |
| 1 and True | True |
| 0 and True | 0 |
| 1 or True | 1 |
| 0 or True | True |
| 1 and False | False |
| 0 and False | 0 |
| 1 or False | 1 |
| 0 or False  | False |
___
| 表达式 | 结果 |
| :----- | ------ |
| True and 1 | 1 |
| True and 0 | 0|
| True or 1 | True |
| True or 0 | True |
| False and 1 | False |
| False and 0 | False |
| False or 1 | 1 |
| False or 0 | 0 |

### 三大语句
#### 顺序语句
自上而下执行语句

#### 分支语句
1. if...
2. if...else...
3. if...elif...else...
4. 分支嵌套

#### 循环结构
1. while
2. for...in...
3. for...in...else...，循环正常结束后执行`else`部分。
4. while...else...
5. break，终止循环的执行
6. continue，终止本轮循环的执行
7. range(m, n, s): 生成 m（默认为0） 到 n-1 的整数，整数间隔为 s（默认为1）。
8. 推导式的使用
```python
list1 = [data for data in range(5)]
list1 = [data**2 for data in range(5)]
list1 = [data for data in range(5) if data > 2]
```

### 函数
1. 函数是将具有独立给你的代码块组织成为一个整体，使其具有特殊给你的代码集。函数的作用主要是加强代码的`复用性`，提高程序编写的效率。
2. 无参函数、有参函数、带返回值的函数
```python
def 函数名([参数]):
	函数体
	[return ...]
```
调用格式
```python
[变量=]函数名([参数])
```
3. 若函数没有返回值，使用变量接收时结果为`None`
4. 函数定义时规定的参数为`形参`，函数调用时使用的参数为`实参`，`形参`的`作用域`为函数定义开始到定义结束。
5. 变量的`作用域`可划分为`局部变量`（整个函数内部）和`全局变量`（整个文件）。
6. `局部变量`可添加关键字`global`提升作用域。
7. 定义函数时，在函数名下用一对`"""`进行文档注释。
8. `默认参数`是函数或方法定义时指定形参的值，位置在`位置形参`的后面，调用该函数或方法时可以不指定默认参数的值，也可以指定默认参数的值，指定多个默认参数的值需要从左到右依次赋值。
9. `关键字参数`是在调用函数或方法时为指定名称的形参赋值所对应的实参.`关键字参数`需要在`位置参数`后面；不能对同一形参多次赋值；既可以为位置参数赋值，也可以为默认参数赋值。通常使用关键字参数是解决`默认参数`选择性赋值的问题。
10. `可变参数`是函数或方法定义时用于接收多个实参的形参，接收的多个实参组装成元组对象，定义可变参数的格式是`*args`。可变参数只能定义一个，定义在`位置参数`的后面。`可变参数`定义在`位置参数`后面。
11. `字典参数`是在函数或方法定义时，用于接收若干组未定义直接使用的关键字参数（调用后，会组装成字典对象），对应的形参。其定义格式是`**kwargs`。`字典参数`只能定义一个。
12. 形参定义的顺序：先`位置参数`，再`可变参数`，后`默认参数`，再后`字典参数`。 
13. `匿名函数`，也称`lambda`表达式。
```python
# 方式一
函数名 = lambda [形参] : 返回值
结果 = 函数名([实参])

# 方式二
结果 = (lambda [形参] : 返回值)([实参])
```

### 面向对象
#### 类和对象
1. `类`是一系列事物的统称，包括`成员变量`和`成员方法`，统称`类成员`。
2. `类`的关键字是`class`，命名满足大驼峰命名法。
3. `对象`是`类`的实例，`self`仅出现在成员方法中，指代执行该方法的对象。
4. 类在`__init__(self)`方法中创建对象时初始化公有成员变量；`对象`可以声明`独有变量`；类可以定义属于类的`类变量`，`类变量`可以私有化。
5. 类的方法有`成员方法`、`类方法`、`私有方法`和`静态方法`。
```python
class AAA:
	def bbb(self[,args]):
		'''成员方法'''
		'''实例变量，实例方法，类变量，类方法均可使用'''
		pass
```
___
```python
class AAA:
	@classmethod
	def bbb(cls[,args]):
	'''类方法'''
	'''不能使用实例变量和实例方法'''
	'''可以使用类变量和类变量'''
	pass
```
___
```python
class AAA:
	def __bb(self[,args]):
	'''私有方法'''
	'''只能在类的内部使用'''
	pass
```
___
```python
class AAA:
	@staticmethod
	def bbb([args]):
	'''静态方法'''
	'''一般不访问成员变量和类变量'''
	pass
```
| 成员方法 | 适用范围 |
| ------ | ------ |
| `成员方法` | 只访问`成员变量` |
| `类方法` | 只访问`类变量` |
| `成员方法` | 既访问`成员变量`，又访问`类变量` |
| `静态方法` | 既不访问`成员变量`，又不访问`类变量` |

6. 魔术方法
 - `__init__(self)`，创建对象时初始化公有成员变量。
 - `__str__(self)`，打印对象时自动调用的方法。
 - `__new__(cls, *args, **kwargs)`，创建对象时自动执行（创建对象由`object`类的`__new__`方法执行）。
 - `__del__(self)`，`销毁对象`时自动执行。

7. `==`与`is`的区别：`==`判断的是内容，`is`判断的是地址。
8. 单例设计模式
```python
class AAA:
    # 单例设计模式
    __instance = None
    def __new__(cls, *args, **kwargs):
        if cls.__instance is None:
            cls.__instance = object.__new__(AAA)
        return cls.__instance
```

#### 封装
1. 封装是对类成员进行访问控制，保护数据不被非法访问。
2. 一般对成员变量进行封装，需要给出访问接口。
```python
class AAA:
	self.__bbb = 1
	def get_bbb(self):
		return self.__bbb
	def set_bbb(self):
		self.__bbb = 2
```

#### 继承
1. 子类可以使用父类的成员变量、类变量、成员方法、类方法、静态方法。子类不能使用父类的私有方法。
2. 获取继承关系的属性`__mro__`。
3. 重写：子类重新定义与父类相同的成员方法。
4. 子类中访问父类被重写的方法
```python
1. 父类名.方法名(对象)
2. super(本类名, 对象).方法名()
3. super().方法名()
```
5. `python`支持`多继承`，访问父类成员时遇到`冲突`，访问继承的第一个父类的成员。

#### 多态
1. 父类的引用指向子类对象。不同子类调用相同的父类方法，执行结果不同。
2. 鸭子类型，类与类之间不用共同继承一个父类，只需要将它们做得像一种事物即可。
3. Duck typing 这个概念来源于美国印第安纳州的诗人詹姆斯·惠特科姆·莱利（James Whitcomb Riley,1849- 1916）的诗句：”When I see a bird that walks like a duck and swims like a duck and quacks like a duck, I call that bird a duck.” 

### 引用
1. 引用是一种变量指向数据存储空间的现象，内存地址是数据在物理内存中的存储位置，引用地址是对象在内存中的描述性地址。
2. 相同数据在内存空间中仅占用一个存储空间。
3. 获取内存存储地址`id()`。
4. 使用`固定内存地址`存储数据如下：-5到256的整数、True和False、由字母、数字、下滑线组成的字符串；使用`临时内存地址`存储数据如下：小于-5后大于256的整数、所有小数、包含字母、数字、下滑线之外的字符组成的字符串。
5. 无变量引用时，列表、集合、字典、对象保存在临时引用地址中，该引用地址可以反复使用；有变量引用时，列表、集合、字典、对象保存在独立引用地址中，该引用地址专用。
6. 列表变量、集合变量、字典变量指向引用地址，该引用地址保存存储信息的内存地址。当存储空间不足时，会申请新的内存地址，并更新引用地址所指向的内存地址，重新申请的内存地址将复制原始内存地址中的数据。
7. 空元组（无数据）：空元组指向统一的独立引用地址，所有空元组共用同一个引用地址。非空元组（有数据）：非空元组保存在独立引用地址中，每个元组对象具有独立引用地址，该引用地址保存存储信息的内存地址，元组创建的同时存储的数据已经固定，内存结构也固定。
8. 元组中的数据如果是引用类型的，对应的数据可以在自身的内存地址中进行数据变更，对元组不影响。
9. 对象中的变量是通过引用地址的形式查找真实数据。对象中的变量存储形式是一个字典的形式，对变量的操作参照字典的操作方式，变量名为字典的key，变量值为字典的value。
10. 可变类型数据：列表、集合、字典和对象；不可变类型数据：数值、字符串、布尔和元组。
11.  变量的引用和定义的区别。

### 文件
#### 文件打开和关闭
```python
# 方式一
file = open(file, mode='r', buffering=None, encoding=None, errors=None, newline=None, closefd=True)
file.close()   # 文件不用后需关闭，否则会造成内存泄漏问题

# 方式二
with open(...) as file:
    pass
```

#### 文件读写模式
1. 官方文档：
| Character | Meaning |
| ------ | ------ |
| 'r' | open for reading (default) |
| 'w'  | open for writing, truncating the file first |
| 'x' | create a new file and open it for writing |
| 'a' | open for writing, appending to the end of the file if it exists |
| 'b' | binary mode |
| 't' | text mode (default) |
| '+' | open a disk file for updating (reading and writing) |
| 'U' | universal newline mode (deprecated) |

2. 翻译：
(1). `rb`，读字节，文件不存在报错。
(2). `wb`，写字节，每次调用会覆盖原文件，文件不存在会新建。
(3). `ab`，追加写字节，写入信息会追加到文件末尾，文件不存在会新建。
(4). `rb+`，读、写字节，文件不存在会报错。
(5). `wb+`，读、写字节，每次调用会覆盖原文件，文件不存在会新建。
(6). `ab+`，读、追加写字节，写入信息会追加到文件末尾，文件不存在会新建。
(7). `r`，读字符，文件不存会报错。
(8). `w`，写字符，每次调用会覆盖原文件，文件不存在会新建。
(9). `a`，追加写字符，写入信息会追加到文件末尾，文件不存在会新建。
(10). `r+`，读、 写字符，文件不存在会报错。
(11). `w+`，读、写字符，每次调用会覆盖原文件，文件不存在会新建。
(12). `a+`，读、追加写字符，写入信息会追加到文件末尾，文件不存在会新建。

#### 读文件
```python
read(self, n: int = -1) -> AnyStr

readable(self) -> bool:

readline(self, limit: int = -1) -> AnyStr:

readlines(self, hint: int = -1) -> List[AnyStr]
```

#### 写文件
```python
writable(self) -> bool

write(self, s: AnyStr) -> int

writelines(self, lines: List[AnyStr]) -> None
```

### 异常处理
1. 异常处理格式
```python
try:
	# 可能引发异常现象的代码
	pass
except:
	# 出现异常时执行的代码
	# 可有多个 except 代码块，但只执行一条 except 代码块
	# 一般格式：except 异常类名[ as 变量名]
	# 一般捕获异常类型从小到大
	# Exception 类是所有异常类的父类
	pass
else:
	# 未出现异常时执行的代码
	pass
finally:
	# try 代码块结束时执行的代码
	pass
```

2. 异常抛出格式
```python
raise 异常类对象
```

3. 自定义异常
```python
class AAA(Exception):
	""" AAA 为自定义异常类名"""
	pass
```
### 模块和包
1. 导入模块的方式
```python
import {模块名}   # 全部导入
from {模块名} import {资源名称}   # 局部导入
# 资源名称包括：类名、函数和全局变量
```
2. 局部导入资源访问控制
```python
from {模块名称} import *
```
```python
__al__ = ["{资源名称}", "{资源名称}"]
```
3. 屏蔽文件的执行代码
```python
if __name__ = "__main__":
	pass
```
4. 模块资源运行工作原理：第一次导入资源文件生成`.pyc`缓存文件。 
5. `包`是项目结构中的目录，用于文件分层管理。

### Tips

1. 超长行处理

 - 换行处使用`\`
 - 对整体添加`()`，`()`中随意换行

2. `import this`
```python
In [1]: import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```