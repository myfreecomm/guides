# Style

A guide for programming in style.

In addition to the general guidelines below, we also have the following more detailed, language/framework-specific style guides:

- [Ruby](/style/ruby)

## Formatting

- Avoid inline comments.
- Break long lines after 120 characters.
- Delete trailing whitespace.
- Don't include spaces after (, [ or before ], ).
- Don't misspell.
- Don't vertically align tokens on consecutive lines. # Hugo: I don't like this rule. I think vertically align tokens produces a better reading experience and we have plugins for editors that make it easy with multi-line editing
- If you break up a hash, keep the elements on their own lines and closing curly brace on its own line.
- Indent continued lines two spaces.
- Indent private methods equal to public methods.
- If you break up a chain of method invocations, keep each method invocation on its own line. Place the . at the end of each line, except the last. [Example](https://github.com/thoughtbot/guides/blob/master/style/ruby/sample.rb#L11). # TODO: change it for our own example
- Use 2 space indentation (no tabs).
- Use an empty line between methods.
- Use empty lines around multi-line blocks.
- Use spaces around operators, except for unary operators, such as !.
- Use spaces after commas, after colons and semicolons, around { and before }.
- Use [Unix-style line endings](http://unix.stackexchange.com/questions/23903/should-i-end-my-text-script-files-with-a-newline) (\n).
- Use [uppercase for SQL key words and lowercase for SQL identifiers](http://www.postgresql.org/docs/9.4/static/sql-syntax-lexical.html#SQL-SYNTAX-IDENTIFIERS).

## EditorConfig

We have a [.editorconfig](/style/.editorconfig). Use it.
