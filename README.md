# NAME

Dist::Zilla::Plugin::Test::Kwalitee::Extra - Dist::Zilla plugin for Test::Kwalitee::Extra

# VERSION

version v0.2.1

# SYNOPSIS

In your `dist.ini`,

    [Test::Kwalitee::Extra]
    arg = !has_example

If you want to avoid network access

    [Test::Kwalitee::Extra]
    arg = !prereq_matches_use

# DESCRIPTION

This module is a [Dist::Zilla](https://metacpan.org/pod/Dist::Zilla) plugin for [Test::Kwalitee::Extra](https://metacpan.org/pod/Test::Kwalitee::Extra). It creates `xt/release/kwalitee.t` to call [Test::Kwalitee::Extra](https://metacpan.org/pod/Test::Kwalitee::Extra).

Most part of codes and tests are identical to [Dist::Zilla::Plugin::Test::Kwalitee](https://metacpan.org/pod/Dist::Zilla::Plugin::Test::Kwalitee). Only the followings are changed points.

- Use [Test::Kwalitee::Extra](https://metacpan.org/pod/Test::Kwalitee::Extra) instead of [Test::Kwalitee](https://metacpan.org/pod/Test::Kwalitee).
- Change variable and configuration names.
- Arguments are passed to Test::Kwalitee::Extra as it is. [Dist::Zilla::Plugin::Test::Kwalitee](https://metacpan.org/pod/Dist::Zilla::Plugin::Test::Kwalitee) adds prefix `-` to disable tests.
- Test for more indicators.

# OPTIONS

- `arg`

    They are passed through to [Test::Kwalitee::Extra](https://metacpan.org/pod/Test::Kwalitee::Extra).

# METHODS

The following methods are overridden.

- `mvp_multivalue_args`

    Declare `arg`.

- `gather_files`

    Create `xt/release/kwalitee.t`.

# NAME

Dist::Zilla::Plugin::Test::Kwalitee::Extra - Dist::Zilla plugin for Test::Kwalitee::Extra

# CAVEATS

An optional indicator `prereq_matches_use` and an experimental indicator `build_prereq_matches_use` require HTTP access to [MetaCPAN site](https://metacpan.org/). If you want to avoid it, you can specify excluded indicators like

    # Avoid network access
    [Test::Kwalitee::Extra]
    arg = !prereq_matches_use

    # or, when experimental enabled
    [Test::Kwalitee::Extra]
    arg = :experimental !prereq_matches_use !build_prereq_matches_use

Or mitigate wait by tentative failures to reduce retry counts like

    # Try just one time for each query
    [Test::Kwalitee::Extra]
    arg = :retry 1

# AUTHORS

- [Dist::Zilla::Plugin::Test::Kwalitee](https://metacpan.org/pod/Dist::Zilla::Plugin::Test::Kwalitee) authors
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
