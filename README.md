automated_factory_girl
======================

When you work with complex domain model sometimes it is so tough to build the final object with minimum code possible for configuration. Its time when automated_factory_girl comes in.

To make it clear why we need this i want to start with defining two trends that i am going to use in this document. 

1. ###Effective numbers
numbers which change the result of test are effective. We dont want this number rely on factories files. The reason behind that is so simple changing a number in factories should not affect a test in a file.

2. ###Configurations
This is what i put it into consideration when i implement my factories.

##Defeciencies in factory_girl

```ruby
class Pane
  attr_accessible :title
  has_many :points
end
class Point
  attr_accessible :name, :lat, :lng
  belongs_to :pane
end
factory :pane do
end
factory :point do
end
```
1. ###has_one
I want to configure a point in a pane

2. ###has_many
I want to configure a point with many panes

3. ###just accept domain objects not hashes
