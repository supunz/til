This is how a function call with an ampersand looks like:
```ruby
some_function(&an_object)
```
When used as shown above, the & operator induces a call to to_proc on the argument, and passes the resulting Proc object (explained in the box below) as a block to the method.



What’s a Proc?
A Proc object encapsulates a function or a block in a way that can be passed around in a variable.
We can initialize a Proc with a block like this:

```ruby
mult = Proc.new { |x, y| x*y }
```

And then use the call method to invoke the block.

Therefore,

```ruby
mult.call(4, 5)
```
returns 20.