# trovu-data-user

Template for creating and managing our own user shortcuts, and for advanced settings.

To get started, fork this repository into your own Github account.

## Custom configuration

You may adjust `config.yml` to your needs.

### Namespaces

    namespaces:
    - o
    - en
    - .us
    - github: .
      name: my

This is an array of the [namespaces](https://github.com/trovu/trovu.github.io/wiki/Namespaces) you want to use. Every entry may be

- a string: Then it refers to an (official) site namespace, i.e. one in the [trovu-data](https://github.com/trovu/trovu-data) repository. Shortcuts in there are curated by the Trovu community.
- key/value pairs, then they refer to a custom namespace, e.g. your (or someone else's) user namespace in Github. Every entry must contain:
  - `github:` A Github user name, or a dot
  - (optional) `name:` Some custom name (default: value from `github:`)

The dot will refer to the current github user (where this `config.yml` is located).

### Default keyword

    defaultKeyword: g 

If no keyword is recognized in a query, this one will be used. Useful for setting up a much used shortcut.

#### Language and Country

    language: en

For Wikipedia or dictionaries in your language. Now, using the `w` shortcut will get you to the Wikipedia in your language.

    country: de

For the Ebay, Amazon of your country. Now, `a` will get you to Amazon.de.

## Adding shortcuts

To add a new shortcut, follow the example in [shortcuts/examplekeyword.1.yml](examplekeyword.1.yml):

- create a file with the keyword and the argument number, 
  - for instance create `g.1.yml` for a shortcut with the keyword g and 1 argument.
- inside the created file, place the template url,
  - like in the [given example](shortcuts/examplekeyword.1.yml).

## Using the shortcuts

For instance, if

- your Github user name is `john-doe`
- and you wish your Trovu user namespace to be `john`

then open https://trovu.net/#github=john-doe

Trovu will then also look within `https://raw.githubusercontent.com/john-doe/trovu-data-user/master/` when you send a query.
