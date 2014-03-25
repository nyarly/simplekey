Simplekey is set of shell scripts to try to simplify what can be the very
confusing process of using GnuPG.

In order to simplify things, by necessity it's very opinionated about the
"right" way to use GnuPG.

There are scads of options presented by OpenPGP, which are all part of making
it the flexible and powerful an encryption framework that it is. But it's
extremely complicated to get started with, and that quite reasonable puts
people off.

The philosophic goals here are these:

1. Make GPG as easy to use as possible. The more people using strong
   encryption, the better for everyone.
2. Make the interface itself auditable. This is why this is presented as shell
   scripts rather than e.g. a web service. If you're concerned about what
   Simplekey does, open up the files and read them, or have someone you trust
   read them.
3. Build a guide forward. The simplified interface provided here should be good
   to get started with, and with luck many users will find they never need
   anything beyond what Simplekey provides. If you find that you need to do
   something more, though, the goal is that you have a foundation to start
   with, and some direction on how to proceed.

## Requirements

You'll need gnupg2 installed. Most Linux distros have some variant of

`apt-get install gnupg`

Mac OS X can do

`brew install gnupg`

You'll also need `sh`, `grep` and `sed`. I only mention that because
the requirements have been made intentionally as light as possible.

## Usage:

Simplekey presents a series of subcommands. At present there are two:

```
./simplekey seal <plaintext> <for>
./simplekey open <encrypted>
```

Those are the day to day "encrypt-sign" and "verify-decrypt" operations.

Planned are:

```
./simplekey configure
./simplekey generate
./simplekey trust <users key>
./simplekey revoke
```

These should be the minimal set required to use GPG effectively.

## Related topics

Public key encryption is a fascinating space. It represents a fusion between
challenging math and logic and human interactions which probably can't be
globally "solved." There are a number of problems that simplekey doesn't yet
approach, simply because it isn't yet clear that it *should.* For instance:

* Low confidence key verification via online identities. (But see affirms/)
* Higher security "detached" master keys.
* Key signing parties

## License

This repository contains code specifically put into the public domain.

## Contribution

I'm eagerly hoping for outside review and contribution to this project. The
goals outlined in the introduction are inflexible, though.

Furthermore, be aware that the act of issuing a Pull Request to this repository
contitutes a contribution of the work in the Pull Request into the public
domain.
