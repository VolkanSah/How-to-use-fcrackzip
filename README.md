# Advanced tips and examples for using **fcrackzip**

## Introduction
fcrackzip is a versatile tool for cracking password-protected zip files. Beyond the basic usage, there are several advanced techniques and tips that can help you use the tool more effectively.

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

## Advanced Examples

### 1. Using Custom Character Sets
Specify a custom character set to limit the brute force attack to specific characters:
```sh
fcrackzip -b -c 1234567890 -l 1-4 protected.zip
```
This command limits the attack to numeric characters and checks passwords of length 1 to 4.

### 2. Parallel Processing
Speed up the cracking process by splitting the task across multiple machines or processes. For example, you can divide the character set and length range:
```sh
fcrackzip -b -c abcdefghijklmnopqrstuvwxyz -l 1-3 part1.zip &
fcrackzip -b -c ABCDEFGHIJKLMNOPQRSTUVWXYZ -l 1-3 part2.zip &
```
This runs two processes in parallel, each working on different sets of characters.

### 3. Using Multiple Dictionaries
If you have multiple dictionaries, you can concatenate them and use the combined file:
```sh
cat dict1.txt dict2.txt > combined_dict.txt
fcrackzip -D -p combined_dict.txt protected.zip
```

### 4. Filtering Results with Unzip
Improve accuracy by using unzip to filter out incorrect passwords:
```sh
fcrackzip -u -D -p dictionary.txt protected.zip
```
This ensures only valid passwords are considered.

### 5. Benchmarking
Run a benchmark to see how fast your system can crack passwords:
```sh
fcrackzip -B
```
This can help you estimate how long a full crack might take.

### 6. Specifying Password Length
Limit the password length range to speed up the attack:
```sh
fcrackzip -b -c aA1 -l 4-8 protected.zip
```
This command will only check passwords with lengths between 4 and 8 characters.

### 7. Using Initialization Passwords
If you have a starting point or known part of the password, you can use it to start the attack:
```sh
fcrackzip -b -p knownpart protected.zip
```

### 8. Verbose Mode
Enable verbose mode for more detailed output:
```sh
fcrackzip -v -b -c aA1 -l 1-8 protected.zip
```

### 9. Validating the Algorithm
Sanity-check the algorithm to ensure it's working correctly:
```sh
fcrackzip -V
```

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
