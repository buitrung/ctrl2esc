# ctrl2esc

_Transforming the most useful key **ever** in a more useful one._
<sub>_For vi/Vim/NeoVim addicts at least_.</sub>

<a href="http://www.catonmat.net/blog/why-vim-uses-hjkl-as-arrow-keys/">
    <img src="http://www.catonmat.net/images/why-vim-uses-hjkl/lsi-adm3a-full-keyboard.jpg" alt="ADM-3A terminal">
</a>

## What is it?

- Makes a single tap of `L_CTRL` into `ESC`
- Forked from `https://gitlab.com/interception/linux/plugins/caps2esc` but
  modified for keyboards that already have CTRL in the right place!
- For more in-depth information, see the original repo, the modifications here
  are exceptionally simple ones so most of the information there still applies!

## Dependencies

- [Interception Tools][interception-tools]

## Building

```
$ git clone git@gitlab.com:grimmware/ctrl2esc.git
$ cd ctrl2esc
$ mkdir build
$ cd build
$ cmake ..
$ make
```

## Execution

`ctrl2esc` is an [_Interception Tools_][interception-tools] plugin. A suggested
`udevmon` job configuration is:

```yaml
- JOB: "intercept -g $DEVNODE | ctrl2esc | uinput -d $DEVNODE"
  DEVICE:
    EVENTS:
      EV_KEY: [KEY_CAPSLOCK, KEY_ESC]

```

For more information about the [_Interception Tools_][interception-tools], check
the project's website.

## License

<a href="https://gitlab.com/interception/linux/plugins/caps2esc/blob/master/LICENSE.md">
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/0b/License_icon-mit-2.svg/120px-License_icon-mit-2.svg.png" alt="MIT">
</a>

Copyright © 2017 Francisco Lopes da Silva, ctrl2esc modifications by Matt Carroll

[interception]: https://github.com/oblitum/Interception
[interception-tools]: https://gitlab.com/interception/linux/tools
