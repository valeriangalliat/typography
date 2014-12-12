Typography
==========

> Typography rules for software documentation.

Capitalization
--------------

The first word of a paragraph or title is capitalized, unless it's a
software, command name, or website (more generally, a "brand" name) that
is not capitalized.

Other words of a title are capitalized with the same rules as for a
paragraph (hence, don't capitalize every word).

Titles are not sentences, and don't end with a period. Though, they can
end with a question or exclamation mark.

* > ### This is a title
  >
  > Here is a regular sentence.

  Basic case, nothing special.

* > How to contribute?

  Question as title.

* > ### moreutils extensions
  >
  > moreutils is a collection of Unix commands.

  Title and paragraph beginning with a software name. moreutils is not
  written capitalized so we don't do it either here.

* > ### Publishing on GitHub

  Naturally, we [respect the case](#common-brand-typos) of GitHub name.

* > ### Additions for French developers

  Here, the language/nationality is capitalized in the title, according to
  English typography rules like for a paragraph.

* > ### `ls` on steroids

  [Rules about monospaced font](#monospace) applies.

Slash
-----

When the "operands" of the "slash operator" are single words, don't add
a space around the slash.

When at least one "operand" contains a space, add spaces around the
slash.

* > Debian is a GNU/Linux distribution.

* > The language/nationality is capitalized.

* > This is my email address / JID.

See [rule](http://en.wikipedia.org/wiki/Slash_(punctuation)#In_English_text)
on Wikipedia.

Repository readme
-----------------

[Readme](http://en.wikipedia.org/wiki/README) is a word.

The repository readme (usually `README.md`) must begin with a level 1
heading, with the repository/project name.

The first header may be followed by a small description in a
`<blockquote>` element (or equivalent). Typically in Markdown:

```md
> Short description of the repository.
```

The short description is a sentence, and thus is ended with a period.

When publishing on GitHub, this short description will typically be the
same as the GitHub repository description. Same for gitweb `description`
or `gitweb.description` files.

Also if your software has a [man page](#man-pages), the short
description in the `NAME` section (though, the man page short
description is not capitalized and does not end with a period):

```nroff
.SH NAME
command \- short description of the repository
```

Monospace
---------

Write in a monospaced font (`<code>` element if in HTML) the following
elemnts:

* HTML tag,
* Unix command,
* filename,
* username,
* anything related to code (like environment variables).

For example:

* > You can use the `<code>` element to format some code, like
  > `puts("Hello, world!")`.

* > Don't forget to `cd` in a directory first if you don't want to extract
  > everything in your working directory.

* > Edit `/etc/ssh/ssh_config` and add `someuser` in the `AllowUsers`
  > directive.

### Inline code

When writing inline code (code in the middle of a sentence), respect the
following rules (at least for C-like languages):

* If you write an expression, don't include the semicolon, like
  `puts("Hello, world!")`, or `1.0 + sqrt(4.0)`.
* If you write one or multiple instructions, include the semicolons: `if
  (foo) return bar;`, `foo(); bar();`.

### Environment variables

When referring to an environment variable, don't include any "variable
symbol", like the `$` in shell.

> The `PATH` environment variable.

Common brand typos
------------------

* GitHub <del>Github</del> <del>github</del>,
* JavaScript <del>Javascript</del> <del>javascript</del>,
* Sass <del>SASS</del>,
* YAML <del>YML</del> <del>Yaml</del>,
* Node.js <del>node.js</del> <del>nodejs</del> (can be written Node when
  appropriate),
* npm <del>NPM</del>,
* Markdown <del>markdown</del>,
* makefile <del>Makefile</del> (but a makefile is often named
  `Makefile`),
* man page <del>manpage</del>.

When not sure, always look the official website to find the correct
spelling/capitalization.

### AWK

* When referring to the language, use "AWK".
* When referring to the command, use "`awk`".

### Unix

* When referring to the Unix OS family, write it "Unix".

  > It's a Unix system! I know this!

  You may emphasis the fact you're speaking of the Unix family by using
  the term "Unix-like".

* When referring to the original AT&T UNIX operating system, write it
  "UNIX".

  > UNIX was publically released in 1982 with the System III edition.

### Linux

* When referring to the kernel, use Linux.
* When referring to the operating system, use GNU/Linux.

Though I believe this is only a rule for formal language. IMO, when
chatting directly with other people, it's tolerable to say just Linux to
mean GNU/Linux.

Man pages
---------

See [man-pages(7)](http://man7.org/linux/man-pages/man7/man-pages.7.html)
for conventions on **how** to write man pages (especially the `STYLE
GUIDE` section).

When **referring** to man pages from a regular document (like this
readme), include the man page section number in parentheses after the
man page name, without space. If it's a link, no special formatting is
required, but otherwise, write the man page name in bold.

* > Refer to [man-pages(7)](http://man7.org/linux/man-pages/man7/man-pages.7.html).

* > See **zshbuiltins**(1) for more information.
