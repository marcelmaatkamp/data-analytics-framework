# Data Analytics Framework

## keycloak
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

# Generate documentation
THis is TBD: either or use both pandoc and mdbook. Evaluating on the go.

## pandoc
```
% docker-compose run pandoc
Creating data-analytics-framework_pandoc_run ... done
[WARNING] Could not fetch resource 'info.svg': replacing image with description
```

# mdbook
This will generate documentation

```
% docker-compose run --rm mdbook init      

Creating data-analytics-framework_mdbook_run ... done

Do you want a .gitignore to be created? (y/n)
y
What title would you like to give the book? 
Data Analytics Framework
2021-04-19 06:14:01 [INFO] (mdbook::book::init): Creating a new book with stub content

All done, no errors...
```


# Introduction

This is a sample [GitHub style markdown](https://github.github.com/gfm/) file.
Top level headers are chapters and other headings are for sub-sections.

# Python

* Lists are declared within `[]` and elements are separated by `,`
* Each element can be of any data type, including list data type

## Example

Use `for` loop to iterate over a list.

```python
numbers = [2, 12, 3, 25, 624, 21, 5, 9, 12]
odd_numbers = []
even_numbers = []

for num in numbers:
    odd_numbers.append(num) if(num % 2) else even_numbers.append(num)

print(f'numbers:      {numbers}')
print(f'odd_numbers:  {odd_numbers}')
print(f'even_numbers: {even_numbers}')
```

>This is a quote

>![info](info.svg) This is a note

# Ruby

* Arrays are declared within `[]` and elements are separated by `,`
* Each element can be of any data type, including array data type

## Example

Use `each` method to iterate over an array.

```ruby
numbers = [2, 12, 3, 25, 624, 21, 5, 9, 12]
odd_numbers = []
even_numbers = []

numbers.each { |n| n.even? ? even_numbers.append(n) : odd_numbers.append(n) }

puts "numbers:      #{numbers}"
puts "odd_numbers:  #{odd_numbers}"
puts "even_numbers: #{even_numbers}"
```

# CLI

Executing the Python and Ruby programs mentioned in previous chapters:

```bash
$ python3.7 list_looping.py
numbers:      [2, 12, 3, 25, 624, 21, 5, 9, 12]
odd_numbers:  [3, 25, 21, 5, 9]
even_numbers: [2, 12, 624, 12]

$ ruby array_looping.rb
numbers:      [2, 12, 3, 25, 624, 21, 5, 9, 12]
odd_numbers:  [3, 25, 21, 5, 9]
even_numbers: [2, 12, 624, 12]
```

# Conclusion

This sample file helps you see a demo for `markdown` to `pdf` conversion using `pandoc`.

 * https://learnbyexample.github.io/customizing-pandoc/
 * https://github.com/peaceiris/docker-mdbook
