# gitignore

Effortlessly generate and regenerate `.gitignore` files from the command line using the [github/gitignore](https://github.com/github/gitignore) templates.

The gitignore CLI was created as it was becoming more and more complicated to bootstrap .gitignore files for complex projects. So often you want to build your .gitignore file from a series of templates, but usually, you will also need to add in some of your own custom rules. This then causes complications several years down the line, when you need to update those templates and custom rules, or you need to add extra technologies to your project which require extra .gitignore rules.

The gitignore CLI allows you to easily generate and regenerate your .gitignore anytime you need to update it, without cluttering up your git diffs. You can define your custom rules in a separate .custom.gitignore file, which allows you to easily update and keep track of them. The gitignore CLI will automatically include them into the compiled .gitignore file.

## Installation

### Homebrew

```bash
brew install bilaalrashid/tap/gitignore
```

### Manual

```bash
wget https://raw.githubusercontent.com/bilaalrashid/gitignore/1.0.1/gitignore
```

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

## Deployment

1. Bump `VERSION` in https://github.com/bilaalrashid/gitignore/blob/main/gitignore#L11
2. Create tag in the form `1.0.0`
3. Create release in the form `Version 1.0.0`
4. Bump the version and sha256 hash in https://github.com/bilaalrashid/homebrew-tap/blob/main/Formula/gitignore.rb
```bash
URL=https://github.com/bilaalrashid/gitignore/archive/refs/tags/1.0.0.tar.gz
wget $URL
sha256sum $(basename $URL)
```
5. Bump version in https://github.com/bilaalrashid/gitignore?tab=readme-ov-file#manual
