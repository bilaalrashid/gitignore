# gitignore

Effortlessly generate `.gitignore` files from the command line using the [github/gitignore](https://github.com/github/gitignore) templates.

## Installation

### Homebrew

```bash
brew install bilaalrashid/tap/gitignore
```

### Manual

```bash
wget https://raw.githubusercontent.com/bilaalrashid/gitignore/1.0.1/gitignore
sudo chmod u+x gitignore
sudo mv gitignore /usr/local/bin/gitignore
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
