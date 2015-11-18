# SSH Backgound Task
## Description
ssh cmd hangs when we want to send remote command executing background job in remote side.
Example

```
# Instance A
ssh user@<IP-of-A> "sleep 10 & echo testRemote";
echo 'testLocal'

```
The `testLocal` will be printed out before the `sleep` is finished. However, we have sent the sleep to background.



## Reference
* `ssh -t` [reference](http://unix.stackexchange.com/questions/39605/ssh-command-unexpectedly-continues-on-other-system-after-ssh-terminates/39608#39608). `ssh -T`  [reference](http://stackoverflow.com/questions/17900760/what-is-pseudo-tty-allocation-ssh-and-github)
 * How your process receive signal is related to `-t` conifg
