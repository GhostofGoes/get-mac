# Contributing to getmac

Thanks for taking an interest in this awesome little project. We love
to bring new members into the community, and can always use the help.

## Important resources
* Bug reports and issues: create an issue on [GitHub](https://github.com/GhostofGoes/get-mac/issues)
* Discussion: the [Python Discord server](https://discord.gg/python)
* [PyPI](https://pypi.org/project/get-mac/)


# Where to contribute

### Good for beginners
* Sample collection (see section below)
* Platform testing (see section below)
* Bug reports!
* Documentation (including fixes for grammar and spelling)
* Improving and adding tests for existing samples

### Main areas of focus
* Writing parsers for new commands (Example: `netsh int ipv6`)
* Addressing missing functionality (Example: default interface detection for IPv6 on Windows)
* Adding new features (Example: ability to find MAC by interface index integer)
* Adding tests for internal methods and mocking where neccessary

### Platform testing
Help is dearly needed on testing and rooting out differences in various platforms and configurations.
At a basic level, this involves just running the tests on any platforms you use.
Open issues for any bugs or quirks you discover, or if you're feeling adventerous, fix it yourself!

Any platform is fair game! The following are some highlights or platforms of special interest:
* MacOS/OSX (This requires owning a Mac, and is the area most sorely in need of testing)
* Legacy Windows desktop (7 and 8)
* Windows Server
* Arch Linux
* BSD

### Sample collection
Examples of output of various commands is an easy way contribute that is still incredibly helpful.
1. Run the command
2. Copy/paste the output (or redirect output of command, `tee` is helpful here) into an appropriatly named `.out` file in `samples/`
3. That's it!


# Getting started
1. Create your own fork of the code through GitHub web interface ([Here's a Guide](https://gist.github.com/Chaser324/ce0505fbed06b947d962))
2. Clone the fork to your computer. This can be done using the
[GitHub desktop](https://desktop.github.com/) GUI , `git clone <fork-url>`,
or the Git tools in your favorite editor or IDE.
3. Create and checkout a new branch in the fork with either your username (e.g. "ghostofgoes"),
or the name of the feature or issue you're working on (e.g. "openbsd-support").
Again, this can be done using the GUI, your favorite editor, or `git checkout -b <branch> origin/<branch>`.
4. Create a virtual environment:
    * Linux/OSX (Bash)
        ```bash
        python -m pip install --user -U virtualenv
        mkdir -p ~/.virtualenvs/
        python -m virtualenv ~/.virtualenvs/getmac
        source ~/.virtualenvs/getmac/bin/activate
        ```
    * Windows (PowerShell)
        ```powershell
        python -m pip install --user -U virtualenv
        New-Item -ItemType directory -Path "$Env:USERPROFILE\.virtualenvs"
        python -m virtualenv "$Env:USERPROFILE\.virtualenvs\getmac"
        $Env:USERPROFILE\.virtualenvs\getmac\Scripts\Activate.ps1
        ```
5. Install the package: `python -m pip install -e .`
6. Setup and run the tests:
```bash
python -m pip install --user -U tox
tox
```
7. Write some code! Git commit messages should information about what changed,
and if it's relevant, the rationale (thinking) for the change.
8. Follow the checklist
9. Submit a pull request!

## Code requirements
* Must work under all supported Python versions (2.6+)
* Must work on all supported platforms, if applicable
* Try to match the general code style (loosly PEP8)
* Be respectful.
Memes, references, and jokes are ok.
Explicit language (cursing/swearing), NSFW text/content, or racism are NOT ok.

## Checklist before submitting a pull request
* [ ] Update the [CHANGELOG](CHANGELOG.md) (For non-trivial changes, e.g. changing functionality or adding tests)
* [ ] Add your name to the contributers list in the [README](README.md)
* [ ] All tests pass locally
* [ ] Pylint is happy

# Bug reports
Filing a bug report:

1. Answer these questions:
    * [ ] What version of `getmac` are you using? (`getmac --version`)
    * [ ] What operating system and processor architecture are you using?
    * [ ] What version of Python are you using?
    * [ ] What did you do?
    * [ ] What did you expect to see?
    * [ ] What did you see instead?
2. Put any excessive output into a [GitHub Gist](https://gist.github.com/) and include a link in the issue.
3. Tag the issue with "Bug"

**NOTE**: If the issue is a potential security vulnerability, do *NOT* open an issue!
Instead, email: ghostofgoes(at)gmail(dot)com

# Features and ideas
Ideas for features or other things are welcomed. Open an issue on GitHub
detailing the idea, and tag it appropriatly (e.g. "Feature" for a new feature).