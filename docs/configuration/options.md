Configuration options for isort
========

As a code formatter isort has opinions. However, it also allows you to also have your own. If your opinions disagree with those of isort,
isort will disagree but commit to your way of formatting. To enable this, isort exposes a plethora of options to specify
how you want your imports sorted.

| Name | Type | Default | Python / Config file | CLI | Description |
|Python Version|Str|py3|py_version|--py,--python-version|Tells isort to set the known standard library based on the the specified Python version. Default is to assume any Python 3 version could be the target, and use a union off all stdlib modules across versions. If auto is specified, the version of the interpreter used to run isort (currently: 38) will be used.|
|Force To Top|Frozenset|frozenset()|force_to_top|-t,--top|Force specific imports to the top of their appropriate section.|
|Skip|Frozenset|frozenset({'.venv', '.mypy_cache', 'build', '_build', '.nox', '.git', 'dist', 'node_modules', '.pants.d', '.tox', '.eggs', 'buck-out', '.hg', 'venv'})|skip|-s,--skip|Files that sort imports should skip over. If you want to skip multiple files you should specify twice: --skip file1 --skip file2.|
|Skip Glob|Frozenset|frozenset()|skip_glob|--sg,--skip-glob|Files that sort imports should skip over.|
|Line Length|Int|79|line_length|-l,-w,--line-length,--line-width|The max length of an import line (used for wrapping long imports).|
|Wrap Length|Int|0|wrap_length|--wl,--wrap-length|Specifies how long lines that are wrapped should be, if not set line_length is used. NOTE: wrap_length must be LOWER than or equal to line_length.|
|Line Ending|Str||line_ending|--le,--line-ending|Forces line endings to the specified value. If not set, values will be guessed per-file.|
|Sections|Tuple|('FUTURE', 'STDLIB', 'THIRDPARTY', 'FIRSTPARTY', 'LOCALFOLDER')|sections|**Not Supported**||
|No Sections|Bool|False|no_sections|--ds,--no-sections|Put all imports into the same section bucket|
|Known Future Library|Frozenset|frozenset({'__future__'})|known_future_library|-f,--future|Force sortImports to recognize a module as part of the future compatibility libraries.|
|Known Third Party|Frozenset|frozenset({'google.appengine.api'})|known_third_party|-o,--thirdparty|Force sortImports to recognize a module as being part of a third party library.|
|Known First Party|Frozenset|frozenset()|known_first_party|-p,--project|Force sortImports to recognize a module as being part of the current python project.|
|Known Standard Library|Frozenset|frozenset({'quopri', 'gc', 'sqlite3', 'zipfile', 'enum', 'posix', 'fileinput', 'io', 'pty', 'sched', 'heapq', 'crypt', 'doctest', 'bdb', 'venv', 'symbol', 'operator', 'cgitb', 'typing', 'shelve', 'ipaddress', 'nis', 'gzip', 'zipimport', 'fpectl', 'compileall', 'aifc', 'smtplib', 'difflib', 'grp', 'selectors', 'faulthandler', 'code', 'xml', 'time', 'distutils', 'cmath', 'importlib', 'textwrap', 'pyclbr', 'itertools', 'zipapp', 'pstats', 'keyword', 'pwd', 'inspect', 'csv', 'warnings', 'stringprep', 'cmd', 'decimal', 'termios', 'codeop', 'reprlib', 'os', 'tabnanny', 'syslog', 'errno', 'string', 'types', 'hmac', 'profile', 'fractions', 'formatter', 'curses', 'nntplib', 'pkgutil', 'locale', 'trace', 'telnetlib', 'sndhdr', 'smtpd', 'functools', 'stat', 'binhex', 're', 'tracemalloc', 'getpass', 'signal', 'xdrlib', 'builtins', 'lib2to3', 'pydoc', 'atexit', 'fnmatch', '_dummy_thread', 'msvcrt', 'audioop', 'configparser', 'abc', 'timeit', 'contextlib', 'optparse', 'marshal', 'fcntl', 'tokenize', 'getopt', 'mailbox', 'queue', 'asyncio', 'math', 'subprocess', 'calendar', 'tempfile', 'datetime', 'unittest', 'logging', 'modulefinder', 'select', 'mailcap', 'platform', 'macpath', 'asynchat', 'pathlib', 'wsgiref', 'threading', 'shutil', 'multiprocessing', 'pickletools', 'encodings', 'symtable', 'spwd', 'struct', 'chunk', 'parser', 'copy', 'uuid', 'socketserver', 'cProfile', 'sysconfig', 'netrc', 'tarfile', 'mmap', 'resource', 'bz2', 'concurrent', 'glob', 'linecache', 'email', 'weakref', 'sys', 'collections', 'poplib', 'imghdr', 'sunau', 'site', 'wave', 'tkinter', 'http', 'random', 'pprint', 'ssl', 'dis', 'imaplib', 'winreg', 'filecmp', 'test', 'statistics', 'hashlib', 'plistlib', 'msilib', 'cgi', 'array', 'dbm', 'turtle', 'gettext', 'html', 'traceback', 'numbers', 'base64', 'copyreg', 'mimetypes', 'asyncore', 'zlib', 'shlex', 'tty', 'webbrowser', 'pipes', 'ftplib', 'unicodedata', 'json', 'colorsys', 'xmlrpc', 'ast', 'bisect', '_thread', 'contextvars', 'urllib', 'secrets', 'imp', 'dataclasses', 'ctypes', 'argparse', 'binascii', 'py_compile', 'rlcompleter', 'codecs', 'lzma', 'ossaudiodev', 'turtledemo', 'runpy', 'winsound', 'dummy_threading', 'readline', 'socket', 'uu', 'pdb', 'token', 'pickle', 'ensurepip'})|known_standard_library|-b,--builtin|Force sortImports to recognize a module as part of the python standard library.|
|Known Other|Dict|{}|known_other|**Not Supported**||
|Multi Line Output|Wrapmodes|WrapModes.GRID|multi_line_output|-m,--multi-line|Multi line output (0-grid, 1-vertical, 2-hanging, 3-vert-hanging, 4-vert-grid, 5-vert-grid-grouped, 6-vert-grid-grouped-no-comma).|
|Forced Separate|Tuple|()|forced_separate|**Not Supported**||
|Indent|Str|    |indent|-i,--indent|String to place for indents defaults to "    " (4 spaces).|
|Comment Prefix|Str|  #|comment_prefix|**Not Supported**||
|Length Sort|Bool|False|length_sort|--ls,--length-sort|Sort imports by their string length.|
|Length Sort Sections|Frozenset|frozenset()|length_sort_sections|**Not Supported**||
|Add Imports|Frozenset|frozenset()|add_imports|-a,--add-import|Adds the specified import line to all files, automatically determining correct placement.|
|Remove Imports|Frozenset|frozenset()|remove_imports|--rm,--remove-import|Removes the specified import from all files.|
|Reverse Relative|Bool|False|reverse_relative|--rr,--reverse-relative|Reverse order of relative imports.|
|Force Single Line|Bool|False|force_single_line|--sl,--force-single-line-imports|Forces all from imports to appear on their own line|
|Single Line Exclusions|Tuple|()|single_line_exclusions|--nsl,--single-line-exclusions|One or more modules to exclude from the single line rule.|
|Default Section|Str|FIRSTPARTY|default_section|--sd,--section-default|Sets the default section for imports (by default FIRSTPARTY) options: ('FUTURE', 'STDLIB', 'THIRDPARTY', 'FIRSTPARTY', 'LOCALFOLDER')|
|Import Headings|Dict|{}|import_headings|**Not Supported**||
|Balanced Wrapping|Bool|False|balanced_wrapping|-e,--balanced|Balances wrapping to produce the most consistent line length possible|
|Use Parentheses|Bool|False|use_parentheses|--up,--use-parentheses|Use parenthesis for line continuation on length limit instead of slashes.|
|Order By Type|Bool|True|order_by_type|--ot,--order-by-type|Order imports by type in addition to alphabetically|
|Atomic|Bool|False|atomic|--ac,--atomic|Ensures the output doesn't save if the resulting file contains syntax errors.|
|Lines After Imports|Int|-1|lines_after_imports|--lai,--lines-after-imports||
|Lines Between Sections|Int|1|lines_between_sections|**Not Supported**||
|Lines Between Types|Int|0|lines_between_types|--lbt,--lines-between-types||
|Combine As Imports|Bool|False|combine_as_imports|--ca,--combine-as|Combines as imports on the same line.|
|Combine Star|Bool|False|combine_star|--cs,--combine-star|Ensures that if a star import is present, nothing else is imported from that namespace.|
|Keep Direct And As Imports|Bool|True|keep_direct_and_as_imports|-k,--keep-direct-and-as|Turns off default behavior that removes direct imports when as imports exist.|
|Include Trailing Comma|Bool|False|include_trailing_comma|--tc,--trailing-comma|Includes a trailing comma on multi line imports that include parentheses.|
|From First|Bool|False|from_first|--ff,--from-first|Switches the typical ordering preference, showing from imports first then straight ones.|
|Verbose|Bool|False|verbose|-v,--verbose|Shows verbose output, such as when files are skipped or when a check is successful.|
|Quiet|Bool|False|quiet|-q,--quiet|Shows extra quiet output, only errors are outputted.|
|Force Adds|Bool|False|force_adds|--af,--force-adds|Forces import adds even if the original file is empty.|
|Force Alphabetical Sort Within Sections|Bool|False|force_alphabetical_sort_within_sections|**Not Supported**||
|Force Alphabetical Sort|Bool|False|force_alphabetical_sort|--fass,--force-alphabetical-sort-within-sections|Force all imports to be sorted alphabetically within a section|
|Force Grid Wrap|Int|0|force_grid_wrap|--fgw,--force-grid-wrap|Force number of from imports (defaults to 2) to be grid wrapped regardless of line length|
|Force Sort Within Sections|Bool|False|force_sort_within_sections|--fss,--force-sort-within-sections|Force imports to be sorted by module, independent of import_type|
|Lexicographical|Bool|False|lexicographical|**Not Supported**||
|Ignore Whitespace|Bool|False|ignore_whitespace|--ws,--ignore-whitespace|Tells isort to ignore whitespace differences when --check-only is being used.|
|No Lines Before|Frozenset|frozenset()|no_lines_before|--nlb,--no-lines-before|Sections which should not be split with previous by empty lines|
|No Inline Sort|Bool|False|no_inline_sort|--nis,--no-inline-sort|Leaves `from` imports with multiple imports 'as-is' (e.g. `from foo import a, c ,b`).|
|Ignore Comments|Bool|False|ignore_comments|**Not Supported**||
|Case Sensitive|Bool|False|case_sensitive|--case-sensitive|Tells isort to include casing when sorting module names|
|Sources|Tuple|()|sources|**Not Supported**||
|Virtual Env|Str||virtual_env|--virtual-env|Virtual environment to use for determining whether a package is third-party|
|Conda Env|Str||conda_env|--conda-env|Conda environment to use for determining whether a package is third-party|
|Ensure Newline Before Comments|Bool|False|ensure_newline_before_comments|-n,--ensure-newline-before-comments|Inserts a blank line before a comment following an import.|
|Directory|Str||directory|**Not Supported**||
|Profile|Str||profile|--profile|Base profile type to use for configuration.|
|Check|Bool|False|**Not Supported**|-c,--check-only,--check|Checks the file for unsorted / unformatted imports and prints them to the command line without modifying the file.|
|Write To Stdout|Bool|False|**Not Supported**|-d,--stdout|Force resulting output to stdout, instead of in-place.|
|Show Diff|Bool|False|**Not Supported**|--df,--diff|Prints a diff of all the changes isort would make to a file, instead of changing it in place|
|Jobs|Int|None|**Not Supported**|-j,--jobs|Number of files to process in parallel.|
|Dont Order By Type|Bool|False|**Not Supported**|--dt,--dont-order-by-type|Don't order imports by type in addition to alphabetically|
|Settings Path|*Not Typed*|None|**Not Supported**|--sp,--settings-path,--settings-file,--settings|Explicitly set the settings path or file instead of auto determining based on file location.|
|Show Version|Bool|False|**Not Supported**|-V,--version|Displays the currently installed version of isort.|
|Vn|Str|==SUPPRESS==|**Not Supported**|--vn,--version-number|Returns just the current version number without the logo|
|Filter Files|Bool|False|**Not Supported**|--filter-files|Tells isort to filter files even when they are explicitly passed in as part of the command|
|Files|*Not Typed*|None|**Not Supported**||One or more Python source files that need their imports sorted.|
|Ask To Apply|Bool|False|**Not Supported**|--interactive|Tells isort to apply changes interactively.|
|Show Config|Bool|False|**Not Supported**|--show-config|See isort's determined config, as well as sources of config options.|