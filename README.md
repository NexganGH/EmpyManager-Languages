# EmpyManager-Languages
**Empymanager-Languages** is a collection of [YAML](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started) files used by [EmpyManager](https://empymanager.com/)
Discord bot to localise every message used by the bot. Each server owner will be able to choose their favourite language and that shall be used to display every message.

The default language is en-UK.yaml, and the goal is to translate the bot in as many languages as possible thanks to the help of the community.

As a new language is added, you will be able to use it once the next update has been deployed.

If a message is not available in the selected language, the bot will fall back to using the en-UK.yaml file.

## How to contribute
You can countribute to this repository as you would do with any other Git repository [like this](https://github.com/firstcontributions/first-contributions).

### Naming system
Each file must be named like the language they represent + the code of the country capitalised. For example, for United Kingdom's English: `en-UK.yaml`. Each file should also
contain a flag representing the main country where the subject language is spoke (See en-UK.yaml's [first line](https://github.com/NexganGH/EmpyManager-Languages/blob/f07f3f0ce976f4835898eec845a180d7d62055b9/en-UK.yaml#L1)).

### How to translate
* As you translate to your original language, always use en-UK.yaml as a base for translation and not other languages, as they might be outdated.

* **You should try to preserve as much as possible the original message**. That is, you can of course change the structure of the phrase
to best fit the language, but keep the original formatting, syntax, punctuation, usage of emojis, etc.

* If you don't like a message 
If you wish to change a specific message because you think it is more fitting the bot, do not edit it in the translation, but edit before the original **en-UK.yaml** file.

### How to write a yaml file
You can simply write a line like this:
```yaml
message-to-translate: This is my message.
```

If the first character is special, you should use double quotes:
```yaml
message-to-translate: "%message% is my message."
```
You should also use quotes if the string contains `:`.

To write a multiline message, use a bar:
```yaml
message-to-translate: |
  This is my multiline 
  
  message.
```

### Variables
You will find **variables** in some messages. Those are words surrounded by `%` that
will be replaced by a dynamic string by the bot. For example in : 
```yaml
tempchannel-panel-title: "%owner%'s Private Chat"
```
`%owner%` will be replaced with the owner's name.

Variables shouldn't be translated or edited in any way.