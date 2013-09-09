# NAME

Dist::Zilla::Plugin::Test::Kwalitee::Extra - Dist::Zilla plugin for Test::Kwalitee::Extra

# VERSION

version v0.1.3

# SYNOPSIS

In your `dist.ini`,

    [Test::Kwalitee::Extra]
    arg = !has_example

# DESCRIPTION

This module is a [Dist::Zilla](http://search.cpan.org/perldoc?Dist::Zilla) plugin for [Test::Kwalitee::Extra](http://search.cpan.org/perldoc?Test::Kwalitee::Extra). It creates `xt/release/kwalitee.t` to call [Test::Kwalitee::Extra](http://search.cpan.org/perldoc?Test::Kwalitee::Extra).

Most part of codes and tests are identical to [Dist::Zilla::Plugin::Test::Kwalitee](http://search.cpan.org/perldoc?Dist::Zilla::Plugin::Test::Kwalitee). Only the followings are changed points.

- Use [Test::Kwalitee::Extra](http://search.cpan.org/perldoc?Test::Kwalitee::Extra) instead of [Test::Kwalitee](http://search.cpan.org/perldoc?Test::Kwalitee).
- Change variable and configuration names.
- Arguments are passed to Test::Kwalitee::Extra as it is. [Dist::Zilla::Plugin::Test::Kwalitee](http://search.cpan.org/perldoc?Dist::Zilla::Plugin::Test::Kwalitee) adds prefix `-` to disable tests.
- Test for more indicators.

# OPTIONS

- `arg`

    They are passed through to [Test::Kwalitee::Extra](http://search.cpan.org/perldoc?Test::Kwalitee::Extra).

# METHODS

The following methods are overridden.

- `mvp_multivalue_args`

    Declare `arg`.

- `gather_files`

    Create `xt/release/kwalitee.t`.

# NAME

Dist::Zilla::Plugin::Test::Kwalitee::Extra - Dist::Zilla plugin for Test::Kwalitee::Extra

# AUTHORS

- [Dist::Zilla::Plugin::Test::Kwalitee](http://search.cpan.org/perldoc?Dist::Zilla::Plugin::Test::Kwalitee) authors
- Yasutaka ATARASHI <yakex@cpan.org>

# LICENSE

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.

# AUTHOR

Yasutaka ATARASHI <yakex@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2012 by Yasutaka ATARASHI.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
