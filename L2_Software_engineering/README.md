# Software Engineering Practices

In this lesson, you'll learn about the following practices of software engineering and how they apply in data science.

### Table of Contents

1. [Writing clean and modular code](#clean_modular)
2. [Writing efficient code](#efficient)
3. [Code Refactoring](#refact)
4. [Meaningful documentation](#doc)
5. [Version control](#version)
6. [Testing](#test)
7. [Logging](#log)
8. [Reviews](#review)
9. [Licensing, Authors, and Acknowledgements](#licensing)

## Writing clean and modular code <a name="clean_modular"></a>

*PRODUCTION CODE:* software running on production servers to handle live users and data of the intended audience. Note this is different from production quality code, which describes code that meets expectations in reliability, efficiency, etc., for production. Ideally, all code in production meets these expectations, but this is not always the case.
- *CLEAN:* readable, simple, and concise. A characteristic of production quality code that is crucial for collaboration and maintainability in software development.
- *MODULAR:* logically broken up into functions and modules. Also an important characteristic of production quality code that makes your code more organized, efficient, and reusable.
- *MODULE:* a file. Modules allow code to be reused by encapsulating them into files that can be imported into other files.

### Clean Code
_*Tip: Use meaningful names*_
- _Be descriptive and imply type_ - E.g. for booleans, you can prefix with is_ or has_ to make it clear it is a condition. You can also use part of speech to imply types, like verbs for functions and nouns for variables.
- _Be consistent but clearly differentiate_ - E.g. age_list and age is easier to differentiate than ages and age.
- _Avoid abbreviations and especially single letters_ - (Exception: counters and common math variables) Choosing when these exceptions can be made can be determined based on the audience for your code. If you work with other data scientists, certain variables may be common knowledge. While if you work with full stack engineers, it might be necessary to provide more descriptive names in these cases as well.
- _Long names != descriptive names_ - You should be descriptive, but only with relevant information. E.g. good functions names describe what they do well without including details about implementation or highly specific uses.

_*Tip: Use whitespace properly*_
- _Organize your code with consistent indentation_ - the standard is to use 4 spaces for each indent. You can make this a default in your text editor.
- _Separate sections with blank lines_ to keep your code well organized and readable.
- _Try to limit your lines to around 79 characters_, which is the guideline given in the PEP 8 style guide. In many good text editors, there is a setting to display a subtle line that indicates where the 79 character limit is.

For more guidelines, check out the code [layout section of PEP 8](https://www.python.org/dev/peps/pep-0008/?#code-lay-out).

### Modular Code
_*Tip: DRY (Don't Repeat Yourself)*_
Don't repeat yourself! Modularization allows you to reuse parts of your code. Generalize and consolidate repeated code in functions or loops.

_*Tip: Abstract out logic to improve readability
*_Abstracting out code into a function not only makes it less repetitive, but also improves readability with descriptive function names. Although your code can become more readable when you abstract out logic into functions, it is possible to over-engineer this and have way too many modules, so use your judgement.

_*Tip: Minimize the number of entities (functions, classes, modules, etc.)*_
There are tradeoffs to having function calls instead of inline logic. If you have broken up your code into an unnecessary amount of functions and modules, you'll have to jump around everywhere if you want to view the implementation details for something that may be too small to be worth it. Creating more modules doesn't necessarily result in effective modularization.

_*Tip: Functions should do one thing*_
Each function you write should be focused on doing one thing. If a function is doing multiple things, it becomes more difficult to generalize and reuse. Generally, if there's an "and" in your function name, consider refactoring.

_*Tip: Arbitrary variable names can be more effective in certain functions*_
Arbitrary variable names in general functions can actually make the code more readable.

_*Tip: Try to use fewer than three arguments per function*_
Try to use no more than three arguments when possible. This is not a hard rule and there are times it is more appropriate to use many parameters. But in many cases, it's more effective to use fewer arguments. Remember we are modularizing to simplify our code and make it more efficient to work with. If your function has a lot of parameters, you may want to rethink how you are splitting this up.

## Writing efficient code <a name="efficient"></a>

T

## Code refactoring <a name="refact"></a>

*REFACTORING:* restructuring your code to improve its internal structure, without changing its external functionality. This gives you a chance to clean and modularize your program after you've got it working.
- Since it isn't easy to write your best code while you're still trying to just get it working, allocating time to do this is essential to producing high quality code. Despite the initial time and effort required, this really pays off by speeding up your development time in the long run.
- You become a much stronger programmer when you're constantly looking to improve your code. The more you refactor, the easier it will be to structure and write good code the first time.

### Example of refactoring
A good example of this can be found in the refactoring_wine_quality.ipynb

## Meaningful documentation <a name="doc"></a>

T

## Version control <a name="version"></a>

T

## Testing <a name="test"></a>

T

## Logging <a name="log"></a>

T

## Reviews <a name="review"></a>

T

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Stack Overflow for the data.  You can find the Licensing for the data and other descriptive information at the Kaggle link available [here](https://www.kaggle.com/stackoverflow/so-survey-2017/data).  Otherwise, feel free to use the code here as you would like! 


