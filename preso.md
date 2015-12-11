class: center, middle
# Ruby Code Analyzers *
##### * lightning talk
---
# Who am I

* Name's **Mikhail Bortnyk**
* Ruby developer and team leader in R&R Music Ukraine
* Co-creator of [Kottans school](http://kottans.org)
* Geek, polyglot, software development addict
* github: [@vessi](https://github.com/vessi)
* twitter: [@mikhailbortnyk](https://twitter.com/mikhailbortnyk)
---
# What the hell are code analyzers?

* *Static code analyzis* - type of analyzis software code without executing
* so, *static code analyzer* - software which performs analyzis of another software and gives conclusion according to some rules
---
# What they do?

* they parse source code to build AST (abstract syntax tree)
* they checking AST with different rules (code style guide, metrics, safeness)
* they show their conclusion according to these rules
---
# Why do we need them?

* it's easier to read the code if it's written in same manner
* helps to avoid *"There are more than one way to do this"* Ruby spike pit (better than just style guides)
* lot of usage places: **linting**, comparing with specifications etc
* history of commits contains only logic changes not formatting
* simple understandable automated rules for code
---
Sample 1:
```ruby
def some_funct param, flag = false
  x = if flag then param + 1 else param end
  {:x => param, :y => x}
```
Sample 2:
```ruby
def some_funct(param, flag: false)
  x = flag ? param + 1 : param
  {x: param, y: x}
end
```
---
# Caveats

* sometimes are too restrictive
* very hard to use at the middle of project lifetime
* touches things you don't care at all
---
# What to choose?

* `rubocop` - https://github.com/bbatsov/rubocop
* `rails_best_practices` - https://github.com/railsbp/rails_best_practices
* `rubycritic` - https://github.com/whitesmith/rubycritic
---
class: center, middle
# Demo
---
class: center, middle
# Questions?
---
class: center, middle
# Thank you!
