# simple-eslint
A simple set of .eslint settings 


## Motivation
Linting is a great way to keep your code consistant. In conjunction with [prettier](https://prettier.io/docs/en/editors.html), it is easy to auto clean your code obeying your linting rules. However, this can cause unexpected reformatting of unchanged code when different IDEs interpret non-explicit defined rules differently.


## Anecdote 
This was most noticed with indenting on Switch statements between Atom and VSCode. If a user of VSCode saved a file with a Switch statement where the case statements were indented, it would remove the indent. If a user of Atom then made additional changes to this file, the removed indents will then be returned. This can make for very annoying code reviews with changesets that are just indent. Adding the rule `"indent": ["warn", 2, { "SwitchCase": 1 }],` resolved this back and forth, and both IDEs applied the rules the same. 

