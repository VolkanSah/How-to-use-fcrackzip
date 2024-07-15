
# How to use: fcrackzip (fast password cracker)

## Introduction
fcrackzip is a fast password cracker partially written in assembler. It is capable of cracking password-protected zip files using brute force or dictionary-based attacks, optionally testing results with unzip. Additionally, it can crack cpmask’ed images. This package is useful for pentesters, ethical hackers, and forensics experts.

## Installed Size
81 KB

## How to Install
To install fcrackzip, use the following command:
```sh
sudo apt install fcrackzip
```

## Dependencies
- fcrackzip: A Free/Fast Zip Password Cracker

## Usage
To display help and usage information, run the following command:
```sh
fcrackzip -h
```

### Example Commands
#### Brute Force Attack
To perform a brute force attack, use:
```sh
fcrackzip -b -c aA1 -l 1-8 protected.zip
```
This command will attempt to crack the password of `protected.zip` using a brute force algorithm with a character set including lowercase letters, uppercase letters, and digits, and passwords of length 1 to 8.

#### Dictionary Attack
To perform a dictionary attack, use:
```sh
fcrackzip -D -p dictionary.txt protected.zip
```
This command will use the words from `dictionary.txt` to attempt to crack the password of `protected.zip`.

#### Using Unzip to Validate
To use unzip to weed out wrong passwords, use:
```sh
fcrackzip -u -D -p dictionary.txt protected.zip
```

#### Benchmark
To execute a small benchmark, use:
```sh
fcrackzip -B
```

### Options
- `-b|--brute-force`: Use brute force algorithm.
- `-D|--dictionary`: Use a dictionary.
- `-B|--benchmark`: Execute a small benchmark.
- `-c|--charset characterset`: Use characters from charset.
- `-h|--help`: Show this message.
- `--version`: Show the version of this program.
- `-V|--validate`: Sanity-check the algorithm.
- `-v|--verbose`: Be more verbose.
- `-p|--init-password string`: Use string as initial password/file.
- `-l|--length min-max`: Check password with length min to max.
- `-u|--use-unzip`: Use unzip to weed out wrong passwords.
- `-m|--method num`: Use method number "num" (see below).
- `-2|--modulo r/m`: Only calculate 1/m of the password.
- `file...`: The zipfiles to crack.

### Methods Compiled In
- 0: cpmask
- 1: zip1
- 2: zip2, USE_MULT_TAB (* default)

## fcrackzipinfo
To display information about a zip file, use:
```sh
fcrackzipinfo --help
```

### Example Command
To parse and display information about `protected.zip`, use:
```sh
fcrackzipinfo protected.zip
```

## Credits
fcrackzip and fcrackzipinfo were written by Marc Lehmann. More information can be found at [Marc's website](http://www.goof.com/pcg/marc/).

## Additional Resources
For further details and updates, visit the [fcrackzip project page](http://www.goof.com/pcg/marc/).



## Your Support
If you find this project useful and want to support it, there are several ways to do so:

- If you find the white paper helpful, please ⭐ it on GitHub. This helps make the project more visible and reach more people.
- Become a Follower: If you're interested in updates and future improvements, please follow my GitHub account. This way you'll always stay up-to-date.
- Learn more about my work: I invite you to check out all of my work on GitHub and visit my developer site https://volkansah.github.io. Here you will find detailed information about me and my projects.
- Share the project: If you know someone who could benefit from this project, please share it. The more people who can use it, the better.
**If you appreciate my work and would like to support it, please visit my [GitHub Sponsor page](https://github.com/sponsors/volkansah). Any type of support is warmly welcomed and helps me to further improve and expand my work.**

Thank you for your support! ❤️

##### Copyright S. Volkan Kücükbudak
