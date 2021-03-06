![Supported Python versions](https://img.shields.io/badge/python-2.7-blue.svg)
![Supported OS](https://img.shields.io/badge/Supported%20OS-Linux-yellow.svg)

# pwg

Personal Wordlist Generator - create wordlist of genrated passwords by profile of subject and customizable patterns of passwords.


Description
===========

pwg is extensible and customizable tool that creates personalized password wordlists. pwg uses custom pattern and profile files, that can be edited freely. With the proper use of the functions that available to manipulate the generated password (L33T, Capitalize, reverse, etc.), the patterns file, and the profile, pwg will create the perfect wordlist for the target.

Features
========

- Wordlist generation by profile and pattern file. 

- Regex support for create unique passwords (exrex).

- Calculate number of items in wordlist.

- Define size of words in wordlist.

- Limit worldlist size.


Examples
========

Generat wordlist using profile and pattern files:

```python pwg.py <Pattern_File>  <Profile_File>```

Calculate number of passwords in wordlist:

```python pwg.py -c <Pattern_File>  <Profile_File>```

Generate in quiet mode to improve efficency:

```python pwg.py -q <Pattern_File>  <Profile_File>```

Limit size of wordlist:

```python pwg.py tests/test_patterns.ppwg tests/test_profile.pwg --limit <NUM_OF_PASSWORDS>```

Define size of words in wordlist:

```python pwg.py tests/test_patterns.ppwg tests/test_profile.pwg --size [min:max]```


Functions (1 Argument):

| Function            | Description                              | Arguments   |
|:--------------------|:-----------------------------------------|:------------|
| upper               | Change all letters to upper case.        |             |
| lower               | Change all letters to lower case.        |             |
| scramble            | Scramble string to all its products.     |             |
| title               | Capitalize first letters of words.       |             |
| leet                | Leet words defined by dicitionary.       | radius      |
| strip               | Strip white spaces.                      |             |
| initials            | Initials of the name.                    |             |
| reverse             | Change string to reverse order.          |             |

Special Functions (3 Arguments):

| Function            | Description                              | Arguments                    |
|:--------------------|:-----------------------------------------|:-----------------------------|
| replace             | Replace chars inside the profile field.  | (to_replace, replace_string) |
| add                 | Add string in specified index.           | (string, index)              |
| split               | Split field to words by delimeter        | (delimeter, from_to_index)   |

Installation
============

- Clone this repository
- pip install requirements.txt.
- python ricco.py --help
