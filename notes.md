# Thu Oct 31 17:39:26 EDT 2019

Running the setup script I realized that everybody seems to have their own
preferences for running linux. The core idea is just to run ubuntu bionic
inside a vagrant box, but everything else that happens seems to be particular
to the user's preferences - tools like go or c compiler and text editor.

I have a preference for a pretty vanilla vim setup so I didn't especially like
the config provided by christianang/linux-training-vm.

In fact, seeing this has me wondering - is this a course on learning how to
use C, vim and unix tools as much as it is about actual system programming
topics? This stuff seems super obvious to me, except for the notes about
checking what options your kernel was configured with. None of that means
anything to me at this point.

## bite size linux

### unix permissions

I became interested/confused by the `setuid` and `setgid` bits in file
permissions, which I've never thought about before.

From what I understand, if the `setuid` bit is set, then the executable will
always execute as the owner. Apparently `setgid` has some different behaviours
depending on whether it is set on an executable file, non-executable file, or
a directory, to which Julia Evans says 'why!?'.

### an amazing directory: `/proc`

I've never looked at `/proc/:pid/{stack,maps,exe,status}` before!

# Thu Oct 31 17:59:10 EDT 2019

Tried running some stuff in a docker container, assuming it would be a faster
way to play with Linux. Didn't really work out, got stuck trying to figure out
how to install manpages in such a way that `man proc` would work. It didn't.
