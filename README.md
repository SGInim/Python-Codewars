# Python Codewars
 Training Python with Codewars
 
# Lessons Learned
1) Lots of code can be written in one line <br>
2) Remember you can \(i,j) for (m,n) in foo\. So long as you unpack the same number of values, you can use tuples in your loop! <br> 
3) The backwards **'\\\\'** after an **else** statement lets you continue in the line below! (in case your line is too long)  <br>
4) The default function output that will work if no parameters are passed: def **def example(my_default=None)** <br>
5) The function **ord(i)** takes a character and returns its integer, the function **chr(i)** does the opposite <br> 
6) **list.sort()** is a is an in-place function and does not save anything (None), use **sorted(list)** <br>
7) **list_name.append(x)** gets appended, you don't have to assign it like list_name = list_name.append() <br>
8) **startswith()** and **endswith()** return a boolean <br>
9) Creating a list with new_list = [ #code# ] is called **list comprehension** <br>
10) **list comprehension** admits **else** in this form: a if a else 2 for a in [0,1,0,3]] <br>
11) **%s %d** %(string, number) I can even add conditions into it! <br>
12) **x // 10** to get all digits but the last; **x % 10** to get last digit <br>
13) To call key,value from dict: **my_dict['key'] (value)** <br>
14) **str({}    {}{}).format(x,y,z...)** <br>
15) **str.replace**('to add','to remove', (optional) number of times) <br>
&emsp; **re.sub**(pattern, repl, string, count=0, flags=0) also works~ (check flags syntax) <br>
&emsp; It is also possible to replace a certain length by **s.replace(s[:-4],'#'\\*(len(s)-4))** or **'{message:#>{fill}}'.format(message=s[-4:], fill=len(s))**<br>
    16) **str.translate(None,'replacement')** is like str.replace() but works for multiple replacements. It is used with str.maketrans for multiple s(1,2,3)<br>
    &emsp; 1.characters that need replacement 2.replacement 3.needs to be deleted (optional) e.g.: **s.translate(str.maketrans(\ąćęłńóśźż\, \acelnoszz\))**<br>
    17) **list.index(i,1)** takes an optional parameter, a number, that tells where to start looking <br>
    18) These **'>>,<<'** are called bitwise shift (right,left) operators. Example: 10>>1 which is the same as 10//(2^1) <br>
    19) **s.split('[+=]')** Use brackets '[]' if you want to split by multiple characters <br>
    20) minutes to time: {:02d}:{:02d}'.format(\\*divmod(n, 60)) Choose n. BTW, divmod returns (a // b, x % y)  <br>
    21) How useful **Map** is <br>
    22) In loops, you can do [**1** for i in iterable], useful with sum()! <br>
    23) **eval(str)** lets you evaluate operations as strings (e.g. '1+1') <br>
    24) **enumerate <3**: It always unpacks two values. Discovered it has an optional arg to set count.<br>
    &emsp; enumerate([1,2,3], 1) will start counting indexes at 1 instead of 0<br>
    25) For data analytics: object**.tolist()** will convert pandas.core.series.Series to list type! <br>
    26) **dict.get(key, None)** The second parameter acts as 'else' to be returned if key is not found <br>
    27) **args** are different than **kwargs** in that kwargs are keyword arguments predefined in a function fun(foo=7,var=2) <br>
    28) **all** and **any** return True if all are True or if any of them are True <br>
    29) **zip** joins two or more iterables (of equal length) by index. Turns them into a generator.<br>                                                &emsp; E.g.: a = (\John\, \Charles\, \Mike\)  b = (\Jenny\, \Christy\, \Monica\); zip(a,b) -> (('John', 'Jenny'), ('Charles', 'Christy'), ('Mike', 'Monica')) <br> 
    30) if/else in function: **e.g.:** def find_avg(nums): return np.mean(nums) if **nums** else 0. -> if 'nums' means not empty <br> 
    31) Python lets you **save anything with x outcomes into any x variables** like this: hours,minutes = divmod(70, 60), or b1,b2 = sorted(['black,'brown']) <br>
    32) Never raise an exception: too many problems. But you can **raise ValueError('add whatever here')** <br>
    33) **not n & 1** returns True if even! <br>
    34) from random import **choice**: e.g.: choice('123456') ...3! <br>
    35) **dir(__builtins__)** contains a list of the built-in functions/methods <br>
    36) **bisect** module provides support to keep a sorted order even after inserting elements in a list <br>
    37) Instead of defining a function: **solution*=lambda s:**chr(sum(map(ord,s.upper()))//len(s)) \\*name of function<br>
    38) **Instantiate** in Python is the process of creating an object from a class (like str) <br>
    39) **s.strip()** removes leading and trailing whitespaces! <br>
    40) The beautiful **%%timeit** <br>
    41) To add a **conditional** inside the **f\** function use \\*: f\{}glass{ 'es'**\\*(condition)** }\ <br>
    &emsp; **Note:** very important to use double quotes first and use single ones inside the brackets or **f\** will think you are closing it beforehand<br> 
    42) **Python RegEx** (Regular Expressions) can be used through 're' package. Useful when you need to do a search or match of  a certain pattern. <br> &emsp; Look up examples and syntax. E.g: foo = r'[A-Z]' would contain each uppercase char. Adding ('+') in the end (r'[A-Z]+') will return it by chunks. <br>
    &emsp; Another useful tip to split by x characters: <br>&emsp; **re.findall('.{1,4}', '123456789')** or **re.findall('....','1234567890')** will split by 4 (leaving {1} character hanging on the former and 0 on the latter). <br>
    &emsp; However, if you want the hanging characters to be replace by something: **re.findall(\.{2}\, '12345' + \\\_\)** <br>
    &emsp; From **textwrap import wrap**. Wrap also does the job wrap(s,4)<br>
    &emsp; Also sub is great for replacement: **sub(r'[to look for]','to replace with', s)**<br>
    43) Intelligent way to make sure there's no repeated values: return [c,i for i in enumerate(s) if condition1 **and i not in s[:c]**] <br>
    44) It is possible to create a function that returns a function, by defining another function inside it and then returning that function, <br> &emsp; without calling it (so, with no parenthesis). Then, you will have to save it in a variable to be able to call it. <br> &emsp; E.g.: add_one = add(1)  /n  add_one(3)  --*Where add_one is the function inside your function* <br>
    45) You can create your return inside a list with conditionals, like: [\Escaped!\,  \Caught!\][x.count('.') <= 3], so that the comparator acts as a separator. <br>
    46) Comparators can be chained, so **(n%x)==0 and (n%y)==0** is the same as: **n%x==0==n%y** (latter way better!) <br>
    47) For the exercises that involve going up and then down like the snail, here's a short solution: **return math.ceil((column - night) / (day - night))** <br>
    48) The **set.issubset(set)** method returns True if all elements in (set) are in set. <br>
    49) Python method **exec(s)** lets you run code inside a string! <br>
    50) The **or** can act as en else!! In loops or almost anywhere: for i in [1,2,7,8]: if i % 2 == 0: print(i) or print('no') <br>
    51) Awesome **RegEx** way to insert * into even digits of a string: return **re.sub(r'(?<=[02468])(?=[02468])', '\\*', s)**<br>
    52) Every class (str, int, list, etc.) has its own methods, and they can be called with underscores as well, like **[1,2,3].\\__contains\\__(3)** or **int(8)\\__add\\__(2)** <br>
    53) The new f\ string has format specifiers for types, padding, or aligning, like f'{price:.3}. By default characters are justified to the left, <br> &emsp; but adding > after a semicolon will justify them to the right. <br>
    54) When you need to iterate over an iterable, there's a smart way to **'go back'** to the beginning (key is to find a math operation to get lower indexes): <br>
    &emsp; e.g.1: return the next one! color = ['green', 'yellow', 'red'] return color[(color.index(current) +1) % len(color)].  **modulo** is the key!<br>
    &emsp; e.g.2: classic rock-paper-scissors: hand = {'rock':0, 'paper':1, 'scissors':2}; results = ['Draw!', 'Player 1 won!', 'Player 2 won!'] [hand[p1] - hand[p2]] <br>
    55) Check if **consecutive:** sorted(n) == list(range(min(n), max(n)+1) <br>
    56) You can **return** your answer **inside a tuple** with conditionals on it! (not just the other way aroud): <br>
    &emsp; return (\AMEX\ if len(s)==15 and s[:2] in (\34\,\37\) else <br>
    &emsp; \Discover\ if len(s)==16 and s.startswith(\6011\) else \\n \Unknown\)<br>
    57) Python has **local and global variables**. A local one is created inside a function and cannot be called outside and viceversa. <br>
    &emsp; But you can access a global variable by typing **global** x (if x was the name of your variable) <br>
    58) If you use ***** in format string the argument input gets split individually! e.g.: return \({}{}) {}{}-{}{} {}\.format(*****n) (function taking a string of n length)<br>
    59) You can save a dictionary with {'black'+'brown': 'dark brown'} and the key counts as one item! (but you can't try to search separately)<br>
    60) The **modulo** defaults to True if result is 0. So, typing **not 2 % 5** will return False <br>
    61) Smart way to return a result for different data types in one line: return **type(data)**( str(data)[::-1] )<br>
    &emsp; Note: Before, I would do it like: if int(str(data)[::-1]), elif float(str(data)[::-1]) and so on. <br>
    62) **alphabet object** without typing it: from string import ascii_lowercase as alphabet <br>
    63) **next**(iterator, default) function retrieves the next item from an iterator object.<br>
    &emsp; E.g.: say you want to return the first non-repeated character in one line: return next(c for c in s if s.count(c) == 1) <br>
    64) According to the **Zen of Python: flat is better than nested**. Ways to flatten a list: <br>
    &emsp; a) **list comprehension** newlist = [item for items in nested_list for item in items] <br>
    &emsp; b) **from itertools import chain** ; newlist = list(chain(\\*nested_list)) **or** newlist = list(chain.from_iterable(nested_list)) <br>
    &emsp; c) **sum function**: newlist = sum(nested_list, []); **reduce function** newlist = reduce(lambda x,y: x+y, nested_list) <br>
    &emsp; d) **import operator** newlist = reduce(operator.add, nested_list). _NOTE: This will be faster than reduce + lambda_ <br>
    65) **Math**: easy and most efficient way to find the number of multiples of **x** in a given number: **number // x**<br>
    66) Python's **accumulate(iterator, [function=addition]) from itertools** takes an iterator and accumulates the function passed (addition if none). <br> 
    &emsp; E.g: example = itertools.accumulate([1,2,3,4,5]) will make the example become [1,3,6,10,15] <br> 
    67) In Python, **Unicode** literals are written as strings prefixed with the 'u' or 'U' character: u'abcdefghijk' <br>
    68) **reduce(fun, seq)** module from **functools** takes in a function and applies it initially to the 1st and 2nd items in the seq, <br>
    &emsp; then applies the generated value with the 3rd item, and so on till there are no items left. <br>
    69) **Ways to multiply an array**: **1)** reduce((lambda x, y: x * y), list1) **2)** numpy.prod(list1)  **3)** list(accumulate(list1, lambda a, b: a * b))[-1] <br>
    70) The **caret symbol ^** does a XOR operation (it results to true if one and only one of the operands is true).<br>
    &emsp; For instance 7^8 = 15 because binary 7 (0111) and binary 8 (1000), so vertically it will result in 1111 (15 in base 2) <br>
    71) **Find closest value in list ways: (k being the value)**:<br> 
    &emsp; A) lst[min(range(len(lst)), key = lambda x: abs(lst[x]-k))] <br>
    &emsp; C) res = min(enumerate(lst), key=lambda x: abs(k - x[1])) <br>
    &emsp; B) with **numpy:** lst = np.asarray(lst);  idx = (np.abs(lst - k)).argmin(); return lst[idx] <br>
    72) Use replace in lambdas if you want to sort a list in a especial way, because it won't replace the actual string! <br>
    73) To check two certain consecutive elements for a condition in an iterator, aside from using enumerate (c+1), <br>
    &emsp; you can define a variable==True and set it to False depending on your condition. <br>
    74) To get all possible combinations of values in a list, **import combinations (from itertools)**. It works like this: <br>
    &emsp; for combo in combinations(lst, 2): print(combo). # 2 for pais, 3 for triplets, etc <br>
    75) You can create a **return with options** that will output whatever **matches**: <br>
    &emsp; {a + b: \addition\, a - b: \subtraction\, a * b: \multiplication\, a / b: \division\}[res] <br>
    76) Fast way to **round** to the nearest x (e.g.: x = 5): **n + (5 - n) % 5**<br>
    77) **Shifting elements** in a list **by 1**: lst = [lst[-1]] + lst[:-1]<br>
    &emsp; But numpy has it even better, **by x**: numpy.roll([1,2,3,4,5], 1)<br>
    78) Clever way (efficiency-speaking) to find missing number in unordered arr of 0 to 100: **5050 - sum(arr)** <br>
    79) In order to **display an image from internet**, import this: **from** IPython.core.display **import** display, HTML, Image <br>
    &emsp; And **use this code**: display(HTML(\https://www.codewars.com/users/Snim/badges/large\)) <br>
    &emsp; Note: Image(image.png) can simply be used if your image is saved locally (same folder as notebook) <br>
    80) **Sort by two keys**: new_list = *sorted(a_list, key=lambda x: (len(x), x))*. Note: first by len and then alphabetically (second 'x')<br>
    81) Python's **from os.path** import **commonprefix** returns prefix shared by all words in list, e.g.: commonprefix(['apple', 'apartment']) will return **ap** <br>
