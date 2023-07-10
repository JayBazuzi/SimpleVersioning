# Simple Versioning 0.1

<a href="https://github.com/JayBazuzi/SimpleVersioning/blob/master/README.md"><img decoding="async" loading="lazy" width="149" height="149" src="https://github.blog/wp-content/uploads/2008/12/forkme_right_gray_6d6d6d.png?resize=149%2C149" class="attachment-full size-full" alt="Improve this page" data-recalc-dims="1"></a>

## Summary

Given a version number MAJOR.MINOR, increment the:

    1. MAJOR version when you make incompatible API changes.
    1. MINOR version when you make backwards-compatible changes.

## Introduction

First, I want to thank [Semantic Versioning](http://semver.org) for giving the world a tool to manage compatibility in software dependencies.

>    _SemVer_ treats releases with new features separately from releases with bug fixes. For dependency management, that distinction isn't important: all that matters is backwards compatibility. "Fixed a bug" and "Added a feature" are both examples of "made the software better", as long as you didn't break something. _SimVer_ is meant to address that difference.

## Simple Versioning Specification (SimVer)

SimVer is [SemVer](http://semver.org) with these modifications:

1. A normal version number MUST take the form X.Y. X is the major version and Y is the minor version.
1. Minor version MUST be incremented for any release which maintains backwards compatibility to the public API.
1. Major version MUST be incremented if any backwards incompatible changes are introduced to the public API.
1. When compatibilty with SemVer tooling is required, it is acceptable to add a '.0' patch version, e.g. 2.1.0, but normally that should be avoided.

## Context

SimVer works best when bugs are relatively rare, when you release quickly/easily/safely, and when you don't maintain many released branches.

## FAQ

### As a consumer of an API, how can I make the most of SimVer?

 - Always accept minor releases (e.g. specify `2.*`)
 - Update early and often.
 - When you see deprecation warnings, update your code as appropriate.

### What kinds of changes make good point releases?

 - Bug fixes.
 - New functionality.
 - Marking old features as deprecated.

### If even the tiniest backwards incompatible changes to the public API require a major version bump, won't I end up at version 42.0 very rapidly?

Maybe. Why is this a problem?

### What about fixing security issues?

I'm tempted to say that security fixes can be minor releases, even if they break compatibility. Thoughts?

## About

The Simple Versioning specification is authored by Jay Bazuzi.

If you'd like to leave feedback, please [tweet](http://twitter.com/jaybazuzi) at me.

## License

[Creative Commons - CC BY 3.0](http://creativecommons.org/licenses/by/3.0/)
