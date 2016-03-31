# Development guides / Ruby

Use [this sample](/style/ruby/.rubocop.yml) file to analyze your code.

- Avoid conditional modifiers (lines that end with conditionals).
- Avoid multiple assignments per line:

```ruby
  one, two = 1, 2
```

- Avoid explicit `return` statements.
- Avoid using semicolons.
- Avoid `unless` with `else`.
- Don't use self explicitly anywhere except class methods:

```ruby
# good
def self.my_class_method
end

# bad
def my_instance_method
  self.my_attribute
end
```

- Prefer &:method_name simple method calls:

```ruby
# good
arr.map(&:name)

# bad
arr.map { |a| a.name }
```

- Prefer `&&` and `||` over `and` and `or`.
- Prefer `!` over `not`.
- Prefer double quotes for strings.
- Prefer `if` over `unless`.
- Prefer `detect` over `find`.
- Prefer `select` over `find_all`.
- Prefer `map` over `collect`.
- Prefer `reduce` over `inject`.
- Prefer `protected` over `private` for non-public `attr_readers`, `attr_writers`, and `attr_accessors`.
- Use `_` for unused block parameters.
- Use {...} for single-line blocks. Use do..end for multi-line blocks.
- Use `?` suffix for predicate methods.
- Use `CamelCase` for classes and modules, `snake_case` for variables and methods, `SCREAMING_SNAKE_CASE` for constants.
- Use `def self.method`, not `def Class.method` or `class << self`.
- Use `each`, not `for`, for iteration.
- Use `def` with parentheses when there are arguments.
