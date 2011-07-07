### git-archive-all.sh

Creates an archive for the entire git superproject, and its submodules

#### Usage

    git-archive-all.sh --version

Prints the program version number on a line by itself and exits.

    git-archive-all.sh --usage|--help|-?

Prints this usage output and exits.

    git-archive-all.sh [--format <fmt>] [--prefix <path>] [--separate|-s] [output_file]

`'--format'` the archive is created with the named git archiver backend. Obviously, this must be a backend that git archive understands. The format defaults to 'tar' if not specified.

`'--prefix'` the archive's superproject and all submodules are created with the <path> prefix named. The default is to not use one.

`'--separate'` or `'-s'` individual archives will be created for each of the superproject itself and its submodules. The default is to concatenate individual archives into one larger archive.

`'output_file'` the resulting archive is created as the file named. This parameter is essentially a path that must be writeable. When combined with `'--separate'` (`'-s'`) this path must refer to a directory.  Without this parameter or when combined with `'--separate'` the resulting archive(s) are named with a dot-separated path of the archived directory and a file extension equal to their format (e.g., `'superdir.submodule1dir.tar'`).

