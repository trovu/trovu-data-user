# trovu-data-user

Template for creating and managing  our own user shortcuts.

To get started, fork this repository.

## Adding shortcuts

To add a new shortcut, follow the example in [g.1.txt](g.1.txt):

- create a file with the keyword and the argument number, 
  - for instance create `g.1.txt` for a shortcut with the keyword g and 1 argument.
- inside the created file, place the template url,
  - like in the [given example](g.1.txt).

## Using the shortcuts

To use them, add the URL to your user repo to Trovu's URL.

For instance, if

- your Github user name is `john-doe`
- and you wish your Trovu user namespace to be `john`

then open https://trovu.net/

- click on the Settings wheel in the namespace bar
- click on *Custom namespaces*
- add 
  - Name: john 
  - Template URL: https://raw.githubusercontent.com/john-doe/trovu-user/master/{%keyword}.{%argumentCount}.txt

