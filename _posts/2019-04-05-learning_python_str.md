---
layout: post
title: learning_python_str
date: 2019-04-05 20:59:41 +0800
tags: [python, str]
categories: 知识总结
author: 痛点就是起点
published: false
---

> 本文为`痛点就是起点`原创文章，可以随意转载，但需注明出处。

### 字符串
* 字符串是一个包含若干个字符并按照一定顺序排列成整体的容器，支持`索引`操作，字符串定义可以是`"xxxx"`,`'xxx'`,`"""xxx"""`,`'''xxx'''`。
* 字符串的一些函数，函数较多，用分割线划分。
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
