

## Comparison operators

The comparison operators are used to determine how two values compare to eachother : *Are these two values equal?* *Is the first value greater than this second value?* *Is the first value less than or equal to the second value?* The result is a Boolean: `True` or `False`.

For instance, let's say I borrowed 13 books at the library and I would like to check if I can rent more given that the maximum amount of books is 15.   



<div class="button-container">     
    <a href="https://app.codeboot.org/5.0.0/?init=.fYm9va3NfZXhhbXBsZS5weQ==~XQAAgABhAQAAAAAAAAAmkEdXvOTiBd_V7Sg2UnzxiMPkGnPkqjQFb6bsOFALs1usuIst7u1dKnSr12RkABkw8rxC5uZF2R3k_d80JTCGKk1cqSLRu68iR3cGLQam7oYOHgSyRUv-KLVXoxsnxg82x0PHN_h2fmcxo7awM2dhsjiuCPpnXAa5Es7TYHq8VT6G2ggDKbp1GC36d_lK_fEZlyd9INBaTxy9fpTMv3N2bhLYG5SelCOFyB2Z95_8YitA.~lang=py-novice.~showLineNumbers=true.~hidden=true.e">         
    <button class="codeboot-button">
      <span>Run example</span>
    </button>     
    </a> 
</div>

```python
MAX_BOOKS = 15    #Note this variable is capitalized because it is a constant.

my_book_count = 13

print("Can I borrow more books?")
print(my_book_count < MAX_BOOKS)

my_book_count +=1
print("Can I borrow more books?")
print(my_book_count < MAX_BOOKS)

my_book_count +=1
print("Can I borrow more books?")
print(my_book_count < MAX_BOOKS)
```



Why use such operators? Those operation will become handy when we introduction conditional statements. This will allow you to establish the relationship between values and be able to implement simple algorithms for decision making. 



### Equality operator `==` 

- The double equal operator`==` compares two operands, if they are equal the result is `True` otherwise the result is `False`. 

| English                               | Python                 |
| ------------------------------------- | ---------------------- |
| Did I borrow 14 books at the library? | `my_book_count == 14`  |
| Is the user's name "Alice"?           | `user_name == "Alice"` |

### Inequality operator != 

- Returns `True` if the operands are not equal and `False` if they are equal 

| English                                                      | Python                       |
| ------------------------------------------------------------ | ---------------------------- |
| I put 10 cookies in my pantry, did my cookie count change?   | `current_cookie_count != 10` |
| I will go to work so long as it's not my birthday. Will I go to work today? | `today != my_birthday`       |



### Greater than `>` 

- Return `True` if the left side operand is greater than the right side operand. Returns `False` otherwise.

| English                                                      | Python                                        |
| ------------------------------------------------------------ | --------------------------------------------- |
| Is Summer McIntosh the first Canadian to win that many gold medals in a single Summer Olympics? | `mcintosh_gold_count > max_canada_gold_count` |



### Greater than or equal `>=`

- Return `True` if the left side operand is greater or equal than the right side operand. Returns `False` otherwise.

| English                                               | Python             |
| ----------------------------------------------------- | ------------------ |
| The passing grade is 60, is Josh passing this course? | `josh_grade >= 60` |



### Less than `<`

- Return `True` if the left side operand is less than the right side operand. Returns `False` otherwise.
- e.g.: `3 < 6 ` result: `True` , `3 < 2`, result: `False`



| English                                                      | Python                                    |
| ------------------------------------------------------------ | ----------------------------------------- |
| Did Summer McIntosh set a new world record in the 400m butterfly? | `mc_intosh_time < world_record_butterfly` |



### Less than or equal `<=`

- Return `True` if the left side operand is less or equal than the right side operand. Returns `False` otherwise.

| English                                              | Python               |
| ---------------------------------------------------- | -------------------- |
| If the temperature outside below the freezing point? | `temperature <= 0.0` |







✍️**Challenge**: Manually execute the operations below and write the expected result. Check your answers by copying the code into a Python editor or terminal. 

<div class="button-container">     
    <a href="https://app.codeboot.org/5.0.0/?init=.fY29tcGFyaXNvbl9jaGFsbGVuZ2VzLnB5~XQAAgADRAAAAAAAAAAARiAToaYFPsVi6rkOY_gtPVhVlVMgMy9wU4vlKRmkTVwrDJddUdRiQhJT3EwSKPiJ8zQXpx7-QY0pis40KWc1I1vWP_QdVVdu0Rerf-ZlAqTc5tMK1TBKFDURcro9LSSbcbpYKde0MLEoG3M-JI9UFvVzEvV_9YtQA.~lang=py-novice.~showLineNumbers=true.~hidden=true.e">         
    <button class="codeboot-button">
      <span>Check answer</span>
    </button>     
    </a> 
</div>

```python
a = 11.999
b = 12
print(a < b)
```

```python
a = (30 / 6) + 3
b = 2**3
print(a == b)
```

```python
a = (25 // 10) * 10 
b = 4**2 + 4
print(a != b)
```

```python
a = 10
b = 7**2 +1
print(a >= b)
```



## Logical operators



Logical operators are used to combine Boolean  values and expressions (`True` or `False`).  They are helpful when programming decision making or creating more complex algorithms. We will learn more about conditional statements in the future. 

There are instances where we need to test if multiple conditions are true at the same time. For example: 

- The relative humidity index must be around 100% **AND** the temperature has to be decreasing for it to rain.
- The oil in the car should be changed every 6 months **OR** every 5,000 km.
- To return a new sweater you must have the receipt **AND NOT** remove the price tag.



The combination of **AND**, **OR**, and **NOT** conditions with the boolean values `True` and `False` is called boolean algebra (or boolean logic), each operation has a special symbol in math and in Python.



| MATH | Python | Operation | Description                             |
| :--- | :----- | :-------- | :-------------------------------------- |
| ⋀    | `and`  | AND       | True when all elements are true.        |
| ⋁    | `or`   | OR        | True when at least one element is true. |
| ¬    | `not`  | NOT       | The inverse of an element.              |

<img src="Images/09_and_or_not.png" height=200/>



## Operator `and`

**Example**

For a meal to be considered a "special", a client must by a pizza and a drink.

| English                                                      | Math                                 | Python                                       |
| ------------------------------------------------------------ | ------------------------------------ | -------------------------------------------- |
| Omnivox is accessible if you are a student  **AND** have the correct password. | access = student ∧∧ correct password | `access = is_student and is_valid_password;` |



### Operator `or`

**Example**

| English                           | Math                    | Python                      |
| --------------------------------- | ----------------------- | --------------------------- |
| Today is a weekday *OR* a weekend | day = weekend ⋁ weekday | `day = weekend or weekday;` |

So, we send our friend out to get pizza and drinks. They come back with pizza and a drink.



### Operator `not`

This operator transforms the variable into **its opposite**. It's also know as **negation**.

**Example**

You are at the library and can only borrow a new book if you do not have any overdue books.

| English                                                 | Math                                 | Python                                        |
| :------------------------------------------------------ | :----------------------------------- | :-------------------------------------------- |
| I can borrow a book if I do *NOT* have an overdue book. | borrow permissible  = ¬ book overdue | `borrow_permissiable = not has_overdue_books` |





✍️**Challenge**: Manually execute the operations below and write the expected result. Check your answers by copying the code into a Python editor or terminal. 

<div class="button-container">     
    <a href="https://app.codeboot.org/5.0.0/?init=.oYm9va3NfZXhhbXBsZS5weQ==~XQAAgABhAQAAAAAAAAAmkEdXvOTiBd_V7Sg2UnzxiMPkGnPkqjQFb6bsOFALs1usuIst7u1dKnSr12RkABkw8rxC5uZF2R3k_d80JTCGKk1cqSLRu68iR3cGLQam7oYOHgSyRUv-KLVXoxsnxg82x0PHN_h2fmcxo7awM2dhsjiuCPpnXAa5Es7TYHq8VT6G2ggDKbp1GC36d_lK_fEZlyd9INBaTxy9fpTMv3N2bhLYG5SelCOFyB2Z95_8YitA.fb2x5bXBpY195ZWFyLnB5~XQAAgAAUAQAAAAAAAAA8mUhJnNeTvgcHkuX6AKbvV44PQEueSO04tYqSeNwNpQw3aHA63QYB9T_K98jsUjlhK0oH-Tj_fEaUlYRNW7jtRw7NdNvfEaww9YUxJMC_6w_QlXlRiFipOXqsfFiEeeQmWuxuBRQBuoD-4j_WkC1MRH9lIei-wS8G8IvFmM-f6DUMXm9z78XVDIK4bFqtoP30gwU=.~lang=py-novice.~showLineNumbers=true.~hidden=true.e">         
    <button class="codeboot-button">
      <span>Check answer</span>
    </button>     
    </a> 
</div>

```python
year = 2024
time_to_next_olympiad  = year % 4
is_summer_olympics = (time_to_next_olympiad == 0)
is_winter_olympics = (time_to_next_olympiad == 2)  and ((year % 2) == 0)
print("True or False, this year is an olympic Games year?")
print(is_summer_olympics or is_winter_olympics)
```

> *The last Summer and Winter Games held in the same year were in Barcelona (Summer) and Albertville (Winter) in 1992. Since then, the Summer and Winter Games are each still held every four years but the Summer Games are celebrated during the first year of an Olympiad and the Winter Games held in the third year.* Source: [International Olympic Committee](https://olympics.com/ioc/faq/history-and-origin-of-the-games/since-when-have-the-summer-and-winter-games-no-longer-been-held-in-the-same-year) algorithm.

