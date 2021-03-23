# maxhotkey-pd
 Pure Data plugin implementing Max-like key&mouse shortcuts.

 Tested on pd vanilla 0.50 win x64. 
 
 Made possible by [Monetus](https://github.com/monetus) and [Seb Shader](https://github.com/sebshader) from the [Pd forum](https://forum.pdpatchrepo.info).

## included

| command | action | done |
|---------|--------|------|
| ctrl+click | toggle edit mode | ✅ | 
| alt+click | open help patch | ✅ |
| ctrl+M | console (Pd window) | ✅ |
| N | new object | ✅ |
| M | message | ✅ |
| B | bang | ✅ |
| I, F | number | ✅ |
| T | toggle | ✅ |
| C | comment | ✅ |
| alt+drag | duplicate | ❌ |
| ctrl+shift+Y | arrange | ❌ |

(replace ctrl with cmd and alt with option for OSX)

## installing

1. Download and copy maxhotkey-plugin.tcl to a folder in Pd's path, like ```Documents/Pd/externals```. See Help > Find externals > Preferences to find your exact paths.

2. Run Pure Data, and the shortcuts should now work!