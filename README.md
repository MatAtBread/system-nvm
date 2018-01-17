# system-nvm
A simple bash script to make the currently selected nvm node installation a system installation

Requires that [nvm is installed](https://github.com/creationix/nvm#install-script)

Typical usage:
```
. system-nvm # Install system-nvm - you can do this in your bash profile or similar

# Install some versions of node and npm using nvm if you haven't already
$ nvm install 8
$ nvm install 9
```

Switch system to v8
```
$ system-nvm 8
Now using node v8.9.4 (npm v5.6.0)
Now using system version of node: v8.9.4 (npm v5.6.0)
$ which node 
/usr/local/bin/node # The "system" node is now active
$ node --version
v8.9.4
```

Switch system to v9
```
$ system-nvm 9
Now using node v9.4.0 (npm v5.6.0)
Now using system version of node: v9.4.0 (npm v5.6.0)
$ which node 
/usr/local/bin/node # The "system" node is now active
$ node --version
v9.4.0
```

Note you can still use `nvm` to set a shell-specific version, `system-nvm` simply sets the system-wide `node` 
and `npm` symlinks to point to to the specified version.

The version you want must have already been installed by `nvm`:
```
$ system-nvm 3
N/A: version "3 -> N/A" is not yet installed.

You need to run "nvm install 3" to install it before using it.
```
