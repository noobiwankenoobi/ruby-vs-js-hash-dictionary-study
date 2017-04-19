# Ruby (Hashes) vs. JavaScript (Dictionaries): Study

Use your favorite search engine and the provided readings to research and
respond to the following questions.

In your responses, be sure to cite any relevant sources you consulted in your
search. We ask you to write responses in your own words in order to see how you
process what you've read. Please do not respond with direct quotes from source
material. Instead, digest what you've read and repeat it in your own voice.

## Required Readings
-   Ruby-Doc.org
    -   [Hash#[]](http://ruby-doc.org/core-2.3.1/Hash.html#method-i-5B-5D)
    -   [Hash#delete](http://ruby-doc.org/core-2.3.1/Hash.html#method-i-5B-5D)
-   [Ruby Programming / Syntax / Literals - Interpolation](https://en.wikibooks.org/wiki/Ruby_Programming/Syntax/Literals#Interpolation)
-   Mozilla Developer Network
    -   [Working with objects - (Deleting properties)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects#Deleting_properties)
    -   [Object.keys()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)
    -   [Template literals](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals)

## Recommended Readings

-   Ruby-Doc.org
    -   [Class: Hash](http://ruby-doc.org/core-2.3.1/Hash.html)
    -   [Class: Symbol](http://ruby-doc.org/core-2.3.1/Symbol.html)
-   Mozilla Developer Network
    -   [Object - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)
    -   [Working with objects - JavaScript | MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Working_with_Objects)

## Creating a Hash in Ruby

Create a hash named `dale` in Ruby with the following key-value pairs.  The keys
should be symbols.

| Key | Value |
| --- | --- |
| family_name | 'gribble' |
| given-name | 'dale' |
| occupation | 'exterminator' |

```ruby

dale = { :family_name => "gribble", :given_name => "dale", :occupation => "exterminator" }

# used:
#ruby-doc.org for Hash#[]
```

## Adding Hash Keys in Ruby
Add a key named `middle name` to `dale` with the string "Alvin" as the value.
Add another key, `hobbies`, to `dale` with an array as the value. The array
should contain two strings, "drinking beer" and "conspiracy theories".  The keys
should be symbols.

```ruby


dale[:middle_name] = "Alvin"

dale[:hobbies] = ["drinking beer", "conspiracy theories"]

# used:
# http://ruby-doc.org/core-2.3.1/Hash.html#method-i-5B-5D
```

## Removing Hash Keys in Ruby

Remove the `middle name` key from `dale`.

```ruby

dale.delete(:middle_name)

# used:
# https://ruby-doc.org/core-1.9.3/Hash.html
```

## Modifying Hash Values in Ruby

Modify `dale` so that the value of the key `family_name` is "Gribble" and the
value of the key `given-name` is "Dale".

```ruby

dale[:family_name] = "Gribble"

dale[:given_name] = "Dale"


# used:
# in-class lesson
```

## Ruby Hash Methods

Using Ruby's Hash methods, set a variable named `dale_keys` to `dale`'s keys.
Additionally, set a variable named `dale_values` to `dale`'s values.'

```ruby

dale_keys = dale.keys
dale_values = dale.values

# used:
# https://ruby-doc.org/core-2.2.0/Hash.html#method-i-values
```

## Accessing Hash Properties and Values

Using Hash methods and string interpolation in Ruby, create a string using
`dale` that equals "My name is Dale Gribble and I'm an exterminator that enjoys
conspiracy theories.".

```ruby

"My name is #{{dale[:given_name]}} #{dale[:family_name]} and I'm an #{dale[:occupation]} that enjoys #{dale[:hobbies(1)]}."

# used:
# https://github.com/noobiwankenoobi/ruby-hash
```

## Creating a Dictionary in JavaScript

Create a dictionary named `hank` in JavaScript with the following key-value
pairs.

| Key | Value |
| --- | --- |
| family_name | 'hill' |
| given-name | 'hank' |
| occupation | 'propane and propane accessories salesman' |

```javascript

const hank = {
  family_name: 'hill',
  given_name: 'hank',
  occupation: 'propane and propane accessories salesman'
}

// used:
// remembered how to do this
```

## Adding Dictionary Properties in JavaScript

Add a property named `middle name` to `hank` with the string "Rutherford" as the
value.  Add another property, `hobbies`, to `hank` with an array as the value.
The array should contain two strings, "drinking beer" and "propane and propane
accessories".

```javascript

hank['middle_name'] = "Rutherford"
hank['hobbies'] = ["drinking beer", "propane and propane accessories"]

// or

hank.push({middle_name: 'Rutherford'})
hank.push({hobbies: ['drinking beer', 'propane and propane accessories']})
// ????

// used:
// http://www.technicalkeeda.com/javascript-tutorials/create-key-value-pair-array-using-javascript
```

## Removing Dictionary Properties in JavaScript

Remove the `middle name` property from `hank`.

```javascript

delete hank.middle_name
delete hank['middle_name']

// used:
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/delete

```

## Modifying Dictionary Values in JavaScript

Modify `hank` so that the value of the key `family_name` is "Hill" and the value
of the key `given-name` is "Hank".

```javascript

hank['family_name'] = 'Hill'
hank['given_name'] = 'Hank'


```

## JavaScript Dictionary Methods

Using JavaScript's Array methods, set a variable named `hankKeys` to `hank`'s
keys.  Additionally, set a variable named `hankValues` to `hanks`'s values.'

```javascript

const hankKeys = Object.keys(hank)

const hankValues = Object.values(hank)

// used:
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/values
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/keys


```

## Accessing Dictionary Properties and Values

Using dictionary methods and template literals in JavaScript, create a string
using `hank` that equals "My name is Hank Hill and I'm a propane and propane
accesories salesman that enjoys drinking beer.".

```javascript

"My name is ${hank['given_name']} ${hank['family_name']} and I'm a ${hank.occupation} that enjoys ${hank.hobbies[0]}."

// tried both ways of doing it in the same line^^

// used:
// Various MDN documentation

```
