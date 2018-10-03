# Plinko
Plinko is a tool that can identify what tests should be ran against a specific product version. These can either be a base version or diff between versions. Version/Diff information must be generated by tools like APIx or CLIx.

Installation
------------
```pip install .```
or
```python setup.py install```


Usage
-----
```usage: plinko [OPTIONS]```

Test Identification
-------------------
Provide a compact diff or version export and pytest --collect-only output to get a file containing all identifiable tests that match the given version/diff. This file location will be printed out at runtime.

**Examples:**

```plinko --help```

```plinko --apix-diff <path/to/diff-comp.yaml> --pytest-export <path/to/collect.txt>```

You can even run Plinko against multiple interfaces at a time.

```plinko --apix-diff <path/to/diff-comp.yaml> --clix-diff <path/to/diff-comp.yaml> --pytest-export <path/to/collect.txt>```

Missing Coverage
----------------
Plinko will also save any functions, without matching tests, to a file. This file location will be printed out at runtime.

Note
----
This project only explicitly supports python 3.7+.