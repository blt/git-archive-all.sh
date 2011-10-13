### git-archive-all.sh

Creates an archive for the entire git superproject, and its submodules

#### Usage

    git-archive-all.sh --version

Prints the program version number on a line by itself and exits.

    git-archive-all.sh --usage|--help|-?

Prints this usage output and exits.

    git-archive-all.sh [--format <fmt>] [--prefix <path>]

`'--format'` the archive is created with the named git archiver
backend. Obviously, this must be a backend that git archive
understands. The format defaults to 'tar' if not specified. (Only
'tar' is supported because I am a bad, lazy man.)

`'--prefix'` the archive's superproject and all submodules are created
with the <path> prefix named. The default is to not use one.

