# Typography

> Typography rules for software documentation.

## Capitalization

The first word of a paragraph or title is capitalized, unless it's a
software, command name, or website (more generally, a "brand" name) that
is not capitalized.

Other words of a title are capitalized with the same rules as for a
paragraph (hence, don't capitalize every word).

Titles are not sentences, and don't end with a period. Though, they can
end with a question or exclamation mark.

> **This is a title**
>
> Here is a regular sentence.

Basic case, nothing special.

> **How to contribute?**

Question as title.

> **moreutils extensions**
>
> moreutils is a collection of Unix commands.

Title and paragraph beginning with a software name. moreutils is not
written capitalized so we don't do it either here.

> **Publishing on GitHub**

Naturally, we [respect the case](#common-brand-typos) of GitHub name.

> **Additions for French developers**

Here, the language/nationality is capitalized in the title, according to
English typography rules like for a paragraph.

> **`ls` on steroids**

[Rules about monospaced font](#monospace) applies.

> **Italic/bold**

When the  first "word" of a title is a "slash expression", capitalize
only the first word if needed.

## Quoted titles, text and code

Adapt the style of quoted content to match that of your document. This
also applies to titles and code.

This rule is inspired by [Scribbr's titles formatting
rules](https://www.scribbr.com/mla/titles/), in particular the "Are
titles capitalized in MLA?" part of the FAQ.

> Use MLA capitalization style even when the original source title uses
> different capitalization.

Only include quotes around the title when it is not a link itself (like
in the paragraph above), otherwise [the link makes for sufficient emphasis](http://writingspaces.org/wwsg/punctuation-hyperlinks).

If quoting the whole title, capitalize the first word like other titles
in this style. However sometimes the title itself fits in my quoting
sentence, and then I like to include it as plain text without
capitalizing it.

> This blog post is an (up-to-date) mix of [How to install NixOS from Linux][nixos-from-linux]
> and [Install NixOS on a So you Start dedicated server][nixos-so-you-start] articles.

[nixos-from-linux]: https://nixos.wiki/wiki/NixOS_Installation_Guide#Installing_from_Linux
[nixos-so-you-start]: http://aborsu.github.io/2015/09/26/Install%20NixOS%20on%20So%20You%20Start%20dedicated%20server/

> If you want to get directly to the heart of the subject, you can jump
> to [another take on accessible permalinks](#another-take-on-accessible-permalinks).
>
> **Another take on accessible permalinks**

## Referencing the source of a quote

End the text of a `<blockquote>` with the source when applicable. The
source needs to start with an em dash.

> This is the content of a quote. It's a beautiful quote!
>
> — [Val, "A collection of nice quotes"](https://github.com/valeriangalliat/typography)

In some Markdown parsers (not on GitHub though), you can use `---` for
this, otherwise use the actual em dash which you can bring up with
<kbd>Option</kbd> + <kbd>Shift</kbd> + <kbd>-</kbd> on a Mac keyboard
layout.

```markdown
> --- [Val, "A collection of nice quotes"](https://github.com/valeriangalliat/typography)
```

Here, I linked the whole reference to the source (not a real source here
obviously), but feel free to add separate links for the author name and
source title.

> — [Val](https://val.codejam.info/), ["A collection of nice quotes"](https://github.com/valeriangalliat/typography)

You can add the source date if relevant.

> — [Val](https://val.codejam.info/), ["A collection of nice quotes"](https://github.com/valeriangalliat/typography), May 14, 2021

When quoting a tweet, use the user handle and date of the tweet.

> TIL rsync can hardlink to previous backups with `--link-dest` and you
> can essentially [recreate macOS Time Machine](https://github.com/cytopia/linux-timemachine/blob/45a03e6aef24d895209c3a588575cac247334918/timemachine#L346)
> with that. This is just beautiful.
>
> — [@valeriangalliat](https://twitter.com/valeriangalliat), [May 13, 2021](https://twitter.com/valeriangalliat/status/1392846380348153860)

I like to link the handle to the user profile and the date to the actual
tweet.

Note how I monospaced `--link-dest` in my quote to match the style of
this document (and also Twitter doesn't allow this kind of rich
text), and instead of dropping the link at the end, I added it to the
relevant part of the text. There's no hard rule for this, but feel free
to do this kind of tasteful alterations that doesn't change the meaning
of the content.

## Slash

When the "operands" of the "slash operator" are single words, don't add
a space around the slash.

When at least one "operand" contains a space, add spaces around the
slash.

> Debian is a GNU/Linux distribution.

> The language/nationality is capitalized.

> This is my email address / JID.

See [rule](http://en.wikipedia.org/wiki/Slash_(punctuation)#In_English_text)
on Wikipedia.

## Italic/bold

Use italic when you want to emphasis text in the "reading flow" (the
expressions are emphasized when reading, but not when globally scanning
the document).

Use bold when you want some words to stand out from the rest of the
text, typically when the reader might search for these words without
reading everything. Use bold with parsimony since it may distract the
reader from what's he's currently reading, by jumping quickly to bold
words.

See [more](http://en.wikipedia.org/wiki/Emphasis_(typography)#Font_styles_and_variants)
on Wikipedia.

When an italic or bold section is followed by punctuation,
[don't include the punctuation in the emphasis][emphasis-punctuation].

[emphasis-punctuation]: https://www.quora.com/In-a-sentence-ending-with-a-bold-or-italicised-word-does-the-period-need-to-be-bold-italicised-too

## Repository readme

[Readme](https://en.wiktionary.org/wiki/readme) is a word.

The repository readme (usually `README.md`) must begin with a level 1
heading, with the repository/project name.

The first header may be followed by a small description in a
`<blockquote>` element (or equivalent). Typically in Markdown:

```markdown
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

## Monospace

Write in a monospaced font (`<code>` element if in HTML) the following
elemnts:

* HTML tag,
* Unix command,
* filename,
* username,
* anything related to code (like an environment variable).

For example:

> You can use the `<code>` element to format some code, like
> `puts("Hello, world!")`.

> Don't forget to `cd` in a directory first if you don't want to extract
> everything in your working directory.

> Edit `/etc/ssh/ssh_config` and add `someuser` in the `AllowUsers`
> directive.

Also use a monospace font (`<kbd>` element if in HTML) for the following
elements:

* physical keys and button labels,
* UI labels (menus and such).

> Press <kbd>Fn Lock</kbd> then <kbd>Shift</kbd> + <kbd>F10</kbd>.

> With the camera off, press <kbd>Right</kbd> + <kbd>DISP.</kbd> +
> <kbd>AF/AE LOCK</kbd> simultaneously.

> For this, you need to open the <kbd>Smart Controls</kbd> panel (e.g.
> by 32:pressing <kbd>B</kbd>).

### Commands

Commands are a particular case because a lot of command-line programs
are named after the command they feature. Though it's not always the
case.

In the case the command and the software "brand" name is the same, you
can ommit the monospaced font when not espacially referring to the
command.

> This program depends on curl and libnotify (for `notify-send`).

  Here, curl is both the "brand" name and command, so we can write it
  as is. Though, libnotify is the software name, but `notify-send` is
  only a command of libnotify.

> `pee` and `sponge` from moreutils are awesome commands!

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
[`man-pages(7)`].

## Notes, warnings

Notes, warnings or other "annotations" are written in bold, followed by
a colon. The following sentence is not capitalized (the beginning of the
sentence is the "note", "warning" or other keyword). Include the colon
in the bold part.

> **Note:** this is a note.

> **Warning:** don't forget to do this.

This rule only applies when the format used have no better semantic for
this. For example, in reST, admonitions are suited for this.

## Common brand typos

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
* Dockerfile <del>dockerfile</del> (because we write Docker, but we
  write `make`)
* man page <del>manpage</del>.

When not sure, always look the official website to find the correct
spelling/capitalization.

### AWK

* When referring to the language, use "AWK".
* When referring to the command, use "`awk`".

### Unix

When referring to the Unix OS family, write it "Unix".

> It's a Unix system! I know this!

You may emphasis the fact you're speaking of the Unix family by using
the term "Unix-like".

When referring to the original AT&T UNIX operating system, write it
"UNIX".

> UNIX was publically released in 1982 with the System III edition.

### Linux

* When referring to the kernel, use Linux.
* When referring to the operating system, use GNU/Linux.

Though I believe this is only a rule for formal language. IMO, when
chatting directly with other people, it's tolerable to say just Linux to
mean GNU/Linux.

## Man pages

See [`man-pages(7)`] for conventions on *how* to write man pages
(especially the `STYLE GUIDE` section).

When *referring* to man pages from a regular document (like this
readme), include the man page section number in parentheses after the
man page name, without space. Write the whole expression as code (this
is the style [adopted on Wikipedia](https://en.wikipedia.org/wiki/Man_page)).

> Refer to [`man-pages(7)`].

> See `zshbuiltins(1)` for more information.

[`man-pages(7)`]: http://man7.org/linux/man-pages/man7/man-pages.7.html

## Code comments

When commenting your code, you might be using single-line comments or
multi-line comments. My recommendation for those would be the following:

* A multi-line comment is always one or multiple sentences, and thus
  should end with a period or other valid punctuation.
* If a single-line comment is a whole sentence, it should also end with
  a period, otherwise it follows the same rules as for [titles](#capitalization).

```js
// This is a sentence where I explain what is going on below.
console.log('Hello, world!')

// Could this also be a question though?
console.log(true)

// Before
doSomething()

// After
doSomethingElse()

/**
 * I like to use this kind of multi-line comment in C-like languages
 * above functions or classes. Note the double star in the beginning. I
 * don't really use that to mark some kind of automated documentation
 * string, I just like the style.
 *
 * While I'm there, I might as well mention that I use Markdown inside
 * code comments if I need to, e.g. when referring to other code like
 * the `doSomethingElse` function which sometimes you can call like
 * `doSomethingElse(true)` that can make it do even something else.
 *
 * When giving multi-line code examples inside a comment, I indent it
 * with an extra 4 spaces (on top of the one space that's always
 * following the comment character), which makes it 5 spaces total.
 *
 *     let a = foo()
 *     console.log(a.someProperty)
 *
 * Very often when I copy/paste stuff from Stack Overflow, I will add
 * the link at the end of my comment like this.
 *
 * See <https://stackoverflow.com/questions/6044330/ffmpeg-c-what-are-pts-and-dts-what-does-this-code-block-do-in-ffmpeg-c>.
 */
function foo () {
  doSomething()

  // That being said, once I'm inside a function, I'm going to use
  // single-line comments even if my comment spans on multiple lines and
  // is a sentence, because I like it better that way, I guess.
  return doSomethingElse()
}
```

In languages that use `#` for comments, for executables that start with
a shebang, I like to follow it with a comment that explains what the
script does.

```sh
#!/bin/sh -e
#
# It looks somewhat like this. Do you like it?
#
# If I'm feeling extra good that day, I might even include an usage
# string in that comment. And when it's about usage strings, I like to
# make them compatible with docopt <http://docopt.org/>, even if I don't
# use it in the project (just for the style).
#
# Usage: mycmd [options] <path>
#
# Options:
#   -h, --help           Show help.
#   --version            Show version.
#   -o, --output=<file>  Output to given file [default: -].
#

path=$1; shift
echo "$path"
```
