# thetacheck

A Python utility for testing apps based on a set of test files. Later succeeded by https://github.com/jbachurski/taucheck/

Should run out-of-the-box on modern Python.

```py
usage: thetacheck.py [-h] [-a APP] [-c CHECKER] [-v] [-ev]
                     [-rd RESULT_DIST] [-l LIMIT] [-x] [-e] [-t]
                     [-s | -S | -N] [-d DIR | -o ONE_FILE]

thetacheck: given an app (-a or --app) and test directory (-d or
--dir) that contains text files named <name>.in and <name>.out
returns statistics of the correctness of the app. Use -h or --help
for help.

options:
  -h, --help            show this help message and exit
  -a APP, --app APP     The application used for testing
  -c CHECKER, --checker CHECKER
                        The application used for checking answers
                        - should accept the .in and .out file
                        contents (as newline-separated strings on
                        the standard input stream) and return
                        status code 0 if the answers are correct
  -v, --verbose         Print out additional data during testing
  -ev, --extra_verbose  Print out even more data during testing
  -rd RESULT_DIST, --result_dist RESULT_DIST
                        Interpret the result/expected output as
                        *one* number and accept the result if it
                        is within the given distance
  -l LIMIT, --limit LIMIT
                        Only run a given amount of tests
  -x, --auto            Automatically locate the tests directory
                        and app
  -e, --empty_means_any
                        If the .out file is empty or missing the
                        result is always counted as correct
  -t, --timer           Print the time taken by the application
  -s, --shuffle         Shuffle the tests randomly
  -S, --do_sort         Sort the tests by size
  -N, --natural_sort    Sort the tests using natural/human sorting
  -d DIR, --dir DIR     The directory where the tests are to be
                        found
  -o ONE_FILE, --one_file ONE_FILE
                        Only run the program for one file (test
                        name is given)
```
