# Development guides / Ruby

## [RuboCop](https://github.com/bbatsov/rubocop)

We made some [modifications](/style/ruby/.rubocop.yml) to rubocop's default
[config file](https://github.com/bbatsov/rubocop/blob/master/config/default.yml).

Do not copy the entire rubocop config file to your project. Use the file containing
our [modifications](/style/ruby/.rubocop.yml).

## [Overcommit](https://github.com/brigade/overcommit)

We use Overcommit to manage git hooks and run some sort of checking into our code before commit
and/or push code to github.

## [Hound](https://houndci.com/repos)

We use Hound to automatically review GitHub pull requests for style guide violations

We use Overcommit to manage git hooks and run some sort of checking into our code before commit
and/or push code to github.

We use a [modified version](/style/ruby/.overcommit.yml) of overcommit's default
[config file](https://github.com/brigade/overcommit/blob/master/config/default.yml).

## Conventions

- Avoid conditional modifiers (lines that end with conditionals).
- Avoid multiple assignments per line:

```ruby
  # bad
  one, two = 1, 2

  # good
  one = 1
  two = 1
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
