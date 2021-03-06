0.12.2
------
* Added parsers for `scientific`, so we can parse decimal places without losing precision.

0.12.1
----
* Fixed the fixed behavior of `notFollowedBy`, which was showing internal state. This had led to unnecessary constraints on internal state that are now removed.

0.12
------
* Fixed the behavior of `notFollowedBy`. This necessitated removing the default implementation, and therefore required a major version bump.

0.11.0.2
--------
* Allow `attoparsec` 0.12

0.11
----
* Mikhail Vorozhtsov refactored `attoparsec` to permit `parsers` instances. Instances added.

0.10.3
------
* Compatibility with ghc 7.8 roles

0.10.2
------
* Documentation fixes

0.10.1.2
--------
* Updated to work with `text` 1.0

0.10.1.1
--------
* 0.10.1 accidentally prevented the orphan instances for ReadP from compiling. Fxed.

0.10.1
------
* Fixed an issue with the expression parser, where it didn't `try` hard enough.
* Added `satisfyRange`
* Fixed a longstanding issue with the char escapes that we inherited from parsec, where ^A and the like were returning 0 not 1.

0.10
----
* Added proper upper bounds for PVP compliance
* Switched to an applicative expression parser

0.9
---
* `instance MonadTrans Unlined`

0.8.3
-----
* Fixed a _major_ performance regression in Text.Parser.Expression

0.8.2
-----
* Added `scalaCommentStyle`.

0.8.1
-----
* Text.Parser.Token.* is now Trustworthy

0.8
---
* Removed the need for `textLiteral`, `textLiteral'` and `identText` by using `fromString`. Use `stringLiteral`, `stringLiteral'`, and `ident` instead respectively.

0.7.1
-----
* Added support for `Text`-based parsing.

0.7
---
* Added `Unlined` to support parsing solely within a line
* Simplified `TokenParsing` instances

0.6
---
* Disallowed nested comments in 'javaCommentStyle'
* More derived instances

0.5.2
-----
* Bugfix in `commaSep1`.

0.5.1
-----
* Taught zeroNumFloat about `0.`.
* Bugfix in `buildExpressionParser`.

0.5
---
* Split out `LookAheadParsing` since it wasn't used by other combinators here and isn't supported by `attoparsec`.

0.4.1
-----
* Added `token` to `TokenParsing`.

0.4
-----
* Updated build system
* Converted various style accessors to lenses and traversals
* More aggressive inlining
* Added CHANGELOG
