#Vexer
Check out [my blog post on Vexer](http://joshualitven.com/vexer/) or [my tutorial on creating anki cards using python](http://joshualitven.com/creating-anki-cards-using-python/) for more information.

Vexer (Vocabulary Expander) creates stylish English vocabulary flash cards for the popular SRS software [Anki](http://ankisrs.net/) using Mac OS X's built-in dictionary.

Vexer uses word definitions to construct cloze-deletioned, multiple-choice Anki cards. Here is an example card with the words *silly*, *funky* and *goofy*:
![Vexer example question](https://raw.githubusercontent.com/jlitven/vexer/master/screenshots/vexer_example_card_question.png?raw=true "Vexer Example Question")

And the corresponding answer:
![Vexer example answer](https://raw.githubusercontent.com/jlitven/vexer/master/screenshots/vexer_example_card_answer.png?raw=true "Vexer Example Answer")

## Version
0.2.1-alpha

## Prerequisites
* Python 2
* Mac OS X 10.5 or higher
* Anki
* `pip` (Python Install Packager)

## Install
`vexer` can be installed using `pip`:
```
sudo pip install vexer
```

## Usage
To create vocabulary cards in Anki, simply call `vexer` with a list of words in the command line or from within a text file:
```
vexer goofy funky silly
```
or
```
vexer my_words.txt
```

You may need to call `sudo vexer` to allow administrator permissions.

_Note: Make sure Anki is closed or else vexer will give you a locked database error._

Upon running for the first time, `vexer` will ask you for your Anki collection path and the name of the deck the words will be added to. These will be stored in a `config.ini` file in the local package directory which you can edit if these parameters change.

You can also include the number of choices in a card using the -n_c (ranging from 2-5) paramater as well as the number of definitions for each part of speech using the -n_d parameter:
```
vexer goofy funky silly -n_c 3 -n_d 2
```

`vexer` stores defaults for these parameters in the `config.ini` file.

For information about all parameters run:
```
vexer --help
```

_Note: Vexer adds the tag `vocabulary` to the Anki cards. Do not edit these tags as vexer uses this tag information._

## Uninstall
`vexer` can be uninstalled using `pip`:
```
sudo pip uninstall vexer
```
