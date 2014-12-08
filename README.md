# Review Abstract Data Structures

##Learning Competencies

* Understand the types of data structures.
* Implement data structures in Ruby.
* Determine when to use a particular data structure.

##Summary

You have now worked extensively with the Array and Hash data structures, and learned a bit about Stack, Queue and Linked List. For this exercise you will delve deeper into another data structure of your choice.

Choose an **Abstract Data Structure** from this list:

 * Map
 * Set
 * String
 * Tree
 * Graph

For more information on these data structures, check the information on [Wikipedia's list of data structures](http://en.wikipedia.org/wiki/List_of_data_structures).

##Restrictions
The following restrictions apply depending on which structure you choose to implement.

####Map
You may not use Ruby's built in Hash type. This one could be tough, but interesting, so let's make a few assumptions. Your Map should be able to use Cohort objects as keys and anything as values. A Cohort class looks like this:

```ruby
class Cohort
  attr_reader :name, :year, :id
  @@id = 0
  def initialize(name, year)
    @name = name
    @year = year
    @id = @@id
    @@id += 1
  end
end
```

And you might use your map class like this:

e.x.
```ruby
fireflies = Cohort.new("Fireflies", 2014)
otters = Cohort.new("Otters", 2014)

favorite_artists = YourMap.new
favorite_artists.add(fireflies, "Miley Cyrus")
favorite_artists.add(otters, "Nickelback")
puts favorite_artists.get(fireflies) #=> "Miley Cyrus"
```

Hint: you might need to figure out a good [hash function](http://en.wikipedia.org/wiki/Hash_table) for Cohorts.

####Set
You may not use Ruby's built-in Set.

####String
You may not use strings internally to represent text. Sound crazy? Read about [Strings](http://en.wikipedia.org/wiki/String_(computer_science)) then check out the `#chr` method on Integer and see if any lightbulbs turn on. The `#ord` method on Ruby's String class could help too.

Your custom string class should be able to _accept_ a Ruby string and create an internal representation of that string via its `#new` method.

It should also have a method to turn your internal representation of that string into a Ruby string (e.g. get a string back out). **However**, your implementation should not store Ruby strings. This will probably be your class's `#to_s` method.

```ruby
example = MyString.new("This ruby string")
example.to_s #=> "This ruby string"
```

Again, you shouldn't need to actually store any string inside your class! Look at the hints above if you're having a hard time wrapping your head around it.

####Tree
There are no restrictions on Tree

####Graph
There are no restrictions on Graph


##Releases

###Release 0 : Describe

Describe the major functions of the data structure in your own words in 3 or 4 sentences.

###Release 1 : Implement

Implement the data structure and its primary functionality, but make sure you're sticking to the restrictions outlined above. Depending on which structure you implement, you'll almost certainly either be using a Hash or Array.

Write specs to show how your implementation works. (Similar to what you saw in the Stack exercise).

###Release 2 : Get real

Describe a 'real' programming problem that you would model with your data structure and how the model represents the problem situation without exposing unnecessary data or methods.

##Resources

*[List of Data Structures](http://en.wikipedia.org/wiki/List_of_data_structures)
