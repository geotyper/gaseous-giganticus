# Gaseous Giganticus 

This program is used to create procedurally generated gas giant planet cubemap
textures for the game Space Nerds In Space.

## Getting Started

1. clone the project
2. Type "make"
3. run "./gaseous-giganticus --help" and do what it says.
4. See also: output of "nroff -man < gaseous-giganticus.1 | more"

The program requires one PNG input image, which should ideally be about 200 pixels wide
and about 1200 pixels tall, and blurred.  It outputs 6 square images that can be thought
of as the faces of a cube, which you can imagine being overinflated until it is a sphere.
The layout of those six output images is as follows:

```
        +------+
        |  4   |
        |      |
        +------+------+------+------+
        |  0   |  1   |  2   |  3   |
        |      |      |      |      |
        +------+------+------+------+
        |  5   |
        |      |
        +------+

```

### Prerequisites

1. libpng

### Coding style

1. Run "git diff | ./checkpatch.pl -".  It will tell you what you did wrong.

TLDR: Tabs, not spaces, snake_case, not CamelCase.

## Contributing

Please read CONTRIBUTING.md

## Authors

* **Stephen M. Cameron**
* **Tobias Simon** (initial author of quaternion library)
* **Jeremy Van Grinsven** (many additions to quaternion library)

## License

GNU GPL v. 2

## Notes

On Sunday, October 21, 2018, this code was split off from the Space
Nerds In Space repository at https://github.com/smcameron/space-nerds-in-space
where the code was originally developed.

An effort was made to preserve the history (git log, etc), and this
effort was 99.9% successful, but there are a few small differences from
the original history. Most significantly, the Makefile does not exist for
most of the history in this repository because the Makefile used in
Space Nerds In Space would have been broken anyway and would have
contained tons of irrelevant cruft. The Makefile in this repository was
added only after the entire gaseous-giganticus history was imported.
Less significantly, a few commits were made out-of-order, and although
the original dates were preserved in the log, checking out a particular
sha you may find some small differences if you compare with what was in
the Space Nerds In Space repository at a corresponding time. At the time
the Makefile was added to this repository, all source files present here
were identical to those also present in the Space Nerds In Space
repository, meaning those small differences were resolved eventually.

