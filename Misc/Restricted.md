# Description 
You 're still trying to collect information for your research on the alien relic. Scientists contained the memories of ancient egyptian mummies into small chips, where they could store and replay them at will. Many of these mummies were part of the battle against the aliens and you suspect their memories may reveal hints to the location of the relic and the underground vessels. You managed to get your hands on one of these chips but after you connected to it, any attempt to access its internal data proved futile. The software containing all these memories seems to be running on a restricted environment which limits your access. Can you find a way to escape the restricted environment ?

# Thoughts 
A docker set up was provided with a restricted user:
```
RUN usermod --shell /bin/rbash restricted
```
Login to the user and see if you can upgrade the shell. https://0xffsec.com/handbook/shells/restricted-shells/
Login with --no profile and tab complete to get the flag (location is randomized in docker. 

```
RUN mv /flag.txt /flag_`cat /dev/urandom | tr -dc 'a-zA-Z0-9' | fold -w 5 | head -n 1`
```
```
ssh restricted@IP -p PORT -t "bash --noprofile"
restricted@box:~$ ls
restricted@nbox:~$ cat /flag_8dpsy 
```

# Solution
## HTB{r35tr1ct10n5_4r3_p0w3r1355}
