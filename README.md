# trovu-user

Template for creating and managing  our own user shortcuts.

To get started, fork this repository.

## Adding shortcuts

To add a new shortcut, follow the example in [shortcuts/g/1.txt](shortcuts/g/1.txt):

- create a new directory using the keyword for its name,
  - for instance create `shortcuts/e/` to have a new shortcut with the keyword `e`.
- create a file inside the directory with the argument number, 
  - for instance create `1.txt` for a shortcut with 1 argument.
- inside the created file, place the template url,
  - like in the [given example](shortcuts/g/1.txt).

## Using the shortcuts

To use them, add the URL to your user repo to Trovu's URL.

For instance, if

- your Github user name is `john-doe`
- and you wish your Trovu user namespace to be `john`

then call Trovu with:
    
    https://trovu.github.io/trovu-web/?#
        namespaces=o,john
        &namespace[john]=https://raw.githubusercontent.com/john-doe/trovu-user/master/shortcuts/{keyword}/{argumentCount}.txt

