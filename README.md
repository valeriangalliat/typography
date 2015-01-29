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

* > ### How to contribute?

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

* > ### Italic/bold

  When the  first "word" of a title is a "slash expression", capitalize
  only the first word if needed.

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

Italic/bold
-----------

Use italic when you want to emphasis text in the "reading flow" (the
expressions are emphased when reading, but not when globally scanning
the document).

Use bold when you want some words to stand out from the rest of the
text, typically when the reader might search for these words without
reading everything. Use bold with parsimony since it may distract the
reader from what's he's currently reading, by jumping quickly to bold
words.

See [more](http://en.wikipedia.org/wiki/Emphasis_(typography)#Font_styles_and_variants)
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
description in the `NAME` section can be the same (though, the man page
short description is not capitalized and does not end with a period):

```nroff
.SH NAME
command \- short description of the repository
```

### Badges

It's common practise in open source projects to add badges next to the
project title, to show the version, code coverage, build status, etc.

The badges should be added after the title, on the same line. If there
are many badges, put them below the title.

Monospace
---------

Write in a monospaced font (`<code>` element if in HTML) the following
elemnts:

* HTML tag,
* Unix command,
* filename,
* username,
* anything related to code (like an environment variable).

For example:

* > You can use the `<code>` element to format some code, like
  > `puts("Hello, world!")`.

* > Don't forget to `cd` in a directory first if you don't want to extract
  > everything in your working directory.

* > Edit `/etc/ssh/ssh_config` and add `someuser` in the `AllowUsers`
  > directive.

### Commands

Commands are a particular case because a lot of command-line programs
are named after the command they feature. Though it's not always the
case.

In the case the command and the software "brand" name is the same, you
can ommit the monospaced font when not espacially referring to the
command.

* > This program depends on curl and libnotify (for `notify-send`).

  Here, curl is both the "brand" name and command, so we can write it
  as is. Though, libnotify is the software name, but `notify-send` is
  only a command of libnotify.

* > `pee` and `sponge` from moreutils are awesome commands!

However, if the program is named after the command, but it's a really
short or ambiguous command (if it's also an English word for example),
it's preferred to refer explicitely to the command, thus using a
monospaced font.

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

**Note:** in a [man page](#man-pages), an environment variable is, well,
a variable, and thus must be written in italics, conforming to
[**man-pages**(7)].

Notes, warnings
---------------

Notes, warnings or other "annotations" are written in bold, followed by
a colon. The following sentence is not capitalized (the beginning of the
sentence is the "note", "warning" or other keyword). Include the colon
in the bold part.

* > **Note:** this is a note.

* > **Warning:** don't forget to do this.

This rule only applies when the format used have no better semantic for
this. For example, in reST, admonitions are suited for this.

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

See [**man-pages**(7)] for conventions on *how* to write man pages
(especially the `STYLE GUIDE` section).

When *referring* to man pages from a regular document (like this
readme), include the man page section number in parentheses after the
man page name, without space. Write the man page name in bold.

* > Refer to [**man-pages**(7)].

* > See **zshbuiltins**(1) for more information.

[ronn](https://github.com/rtomayko/ronn) is a nice software to write man
pages in a friendly Markdown format. Though the RubyGems version is
outdated, you have to use the Git version, which respects the "bold man
page name" convention.

See [sassdocify's man page](https://github.com/SassDoc/sassdocify/blob/master/man/man1/sassdocify.1.ronn)
for a good ronn example.

[**man-pages**(7)]: http://man7.org/linux/man-pages/man7/man-pages.7.html
