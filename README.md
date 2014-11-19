automated_factory_girl
======================

Taking a substential construction logic and encapsulated in a class all of its own is reaponsibility of builder pattern. However factorty girl provides abstract factory pattern in rails. 

As a result, when it comes to writes thousand line of codes for a feature which needs the same construction routine for each scenario automated_factory_girl comes in.

Consider that you are going to build a robot in an advanced project with all of its features. So behaviour testing is a must. For robot construction you need 10 lines of codes to configure a robot then test a specific behaviour. When you 1000 behaviour you have to write 10,000 line of code of same configuration into various files. First concern is DRY. Second concerns is when we need to add another configuration you have to deal with 10,000 lines in your code base. On the other hand, factory_girl has its own defeciencies.

TODO

##Defeciencies in factory_girl

```ruby
class Robot
  attr_accessible :model
  has_many :twists
end
class Twist
  attr_accessible :serial, :height, :width
  belongs_to :model
end
factory :robot do
end
factory :twist do
end
```

1. ####Effective & configuration agents
TODO

2. ####Has_one issue
TODO

3. ####Has_many issue
TODO
