# Build ASCII slugs: implementation

## What the example does

NFKD decomposes accented letters before ASCII filtering. Non-Latin text can become empty, so never use this result as a globally unique identifier.

The public function is `solve(value)`. The JSON input contract can be seen in this concrete example:

```json
"Café & Code"
```

Expected result:

```json
"cafe-code"
```

Run `python3 example.py` for the Python representation of the result. `solution.py` contains the full implementation and can also be imported by another script.

## Scope

The function implements exactly the behavior described above. It does not perform network or filesystem access. Python exceptions indicate unsupported input; the next lesson turns them into a command-line error response. Review the limitations before reusing it in an application.
