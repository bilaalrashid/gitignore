# gitignore

Effortlessly generate `.gitignore` files from the command line using the [github/gitignore](https://github.com/github/gitignore) templates.

## Usage

### Generate

Generates the contents of a `.gitignore` file from specified templates names. To append custom rules to the generated output, an optional `.custom.gitignore` file can be defined in the current working directory. This can be useful when regenerating a `.gitignore` midway through a project. 

```bash
gitignore generate [template] [template] [template] ...
```

#### Example

```bash
$ gitignore generate Swift Global/Xcode Global/macOS > .gitignore
```

### Search

Perform a batch search of queries against all available `.gitignore` templates.

```bash
gitignore search [query] [query] [query] ...
```

#### Example

```bash
$ gitignore search swift xcode mac
Swift
Global/Xcode
Global/Emacs
Global/macOS
```

### List

Lists all available `.gitignore` template files.

```bash
gitignore list
```

### Help

Display help information.

```bash
gitignore help
```

