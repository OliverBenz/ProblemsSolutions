# Proper GREP

## Problem
How to properly use the grep command efficiently.

## How to fix
`grep -rin "STRING" --include \*.h --include *\.cpp`

| Value     | Meaning                    |
| --------- | :-------------------------:|
| grep      | Command                    |
| -r        | recursive search           |
| -i        | ignore case-sensitive      |
| -n        | add line number to result  |
| --include | check specific file format |


