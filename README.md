# TagCollection

![image](https://github.com/jiangxincode/TagCollection/raw/master/screenshots/status.png)

Some tags used by the OmniCppComplete which can auto complete your code.

This TagCollection includes the useful libraries likes:

+ ANSI C(C99)
+ ISO C++(C++11)
+ POSIX
+ MPI(MPI 2.2).

If you have some advises, please tell me, open a issue, give me a pull request, or send me a email. 

Hava a good time on VIM.

+ Aloys
+ jiangxinnju@163.com
 
![image](https://github.com/jiangxincode/TagCollection/raw/master/screenshots/mpi_autocomplete.png)


## Installation

First of all, you should install these tools:

+ [ctags](http://ctags.sourceforge.net/)
+ [OmniCppComplete](http://www.vim.org/scripts/script.php?script_id=1520)

And then you can install the TagCollection

If you use [Vundle](https://github.com/gmarik/vundle),add the following line to your `~/.vimrc`:

```vim
Plugin 'jiangxincode/TagCollection'
```
Then run inside Vim:

```vim
:so ~/.vimrc
:PluginInstall
```

If you use [Pathogen](https://github.com/tpope/vim-pathogen), do this:

```sh
cd ~/.vim/bundle
git clone https://github.com/jiangxincode/TagCollection.git
```

If you are not using any package manager, download the [tarball](https://github.com/jiangxincode/TagCollection/archive/master.tar.gz) and this, but you should modify the the path in the plugin/TagCollection.vim

```sh
cd ~/.vim
tar --strip=1 -zxf TagCollection-master.tar.gz
```

## Configue


## Reference

+ [C standard library](http://en.wikipedia.org/wiki/C_standard_library)
+ [C++ Standard Library](http://en.wikipedia.org/wiki/C%2B%2B_Standard_Library)
+ [C POSIX library](http://en.wikipedia.org/wiki/C_POSIX_library)

## Commands used to product the tags

+ C99(exclude "iso646.h")

```
cd /usr/include/
sudo ctags --c-kinds=+px --c++-kinds=+px --fields=+iafksS --extra=+qf assert.h ctype.h errno.h c++/4.8/tr1/float.h limits.h locale.h math.h setjmp.h signal.h c++/4.8/tr1/stdarg.h linux/stddef.h stdio.h stdlib.h string.h time.h wchar.h wctype.h complex.h fenv.h inttypes.h c++/4.8/tr1/stdbool.h stdint.h tgmath.h
```

+ C++11(exclude "codecvt")

```
cd /usr/include/c++/4.8
sudo ctags --c-kinds=+px --c++-kinds=+px --fields=+iafksS --extra=+qf array bitset deque forward_list list map queue set stack unordered_map unordered_set vector algorithm chrono functional iterator memory stdexcept tuple utility locale string regex fstream iomanip ios iosfwd iostream istream ostream sstream streambuf exception new typeinfo thread mutex condition_variable future complex random valarray numeric 
```

+ posix(exclude "netdb.h", "trace.h")

```
cd /usr/local/openmpi-1.8.4/include
sudo ctags --c-kinds=+px --c++-kinds=+px --fields=+iafksS --extra=+qf aio.h arpa/inet.h cpio.h dirent.h dlfcn.h fcntl.h fmtmsg.h fnmatch.h ftw.h glob.h grp.h iconv.h langinfo.h libgen.h monetary.h mqueue.h net/if.h netdb.h netinet/in.h netinet/tcp.h nl_types.h poll.h pthread.h pwd.h regex.h sched.h search.h semaphore.h spawn.h strings.h stropts.h x86_64-linux-gnu/sys/*.h syslog.h tar.h termios.h ulimit.h unistd.h utime.h utmpx.h wordexp.h
```

+ mpi

```
cd /usr/local/openmpi-1.8.4/include
sudo ctags --c-kinds=+px --c++-kinds=+px --fields=+iafksS --extra=+qf -R *
```

## TODO


## License

The MIT License (MIT)

Copyright (c) 2015 Aloys JiangXin

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
