## Travis Reducer

Test like the following:

```bash
echo "foo foo quux labs foo bar quux" | /home/hduser/travis-reducer/reducer.py
foo     1
foo     1
quux    1
labs    1
foo     1
bar     1
quux    1

hdusermontana@ubuntu:~$ echo "foo foo quux labs foo bar quux" | /home/hduser/travis-reducer/reducer.py | sort -k1,1 | /home/hduser/reducer.py
bar     1
foo     3
labs    1
quux    2

hdusermontana@ubuntu:~$ cat /tmp/gutenberg/20417-8.txt | /home/hduser/mapper.py
 The     1
 Project 1
 Gutenberg       1
 EBook   1
 of      1
 [...]
 (you get the idea)
 ```
