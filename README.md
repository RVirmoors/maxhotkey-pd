# maxhotkey-pd
 Pure Data plugin implementing Max-like key&mouse shortcuts & UI behaviour.

 Tested on pd vanilla 0.52 win x64. 
 
 Made possible by [Monetus](https://github.com/monetus) and [Seb Shader](https://github.com/sebshader) from the [Pd forum](https://forum.pdpatchrepo.info).

## included

| command | action | done |
|---------|--------|------|
| ctrl+click | toggle edit mode | ✅ | 
| alt+click | open help patch | ✅ |
| ctrl+M | console (Pd window) | ✅ |
| double-click | new object | ✅ |
| typing into object box | hide cursor | ✅ |
| N | new object | ✅ |
| M | message | ✅ |
| B | bang | ✅ |
| I, F | number | ✅ |
| T | toggle | ✅ |
| C | comment | ✅ |
| enter | apply object | ❌ |
| alt+drag | duplicate | ❌ |
| ctrl+shift+Y | arrange | ❌ |

(replace ctrl with cmd and alt with option for OSX)

I started this as a complete tcl/tk newbie, so the hard stuff (❌) will take a while to implement. Any contributions are welcome!

## installing

1. Download and copy `maxhotkey-plugin.tcl` to a folder in Pd's path, like ```Documents/Pd/externals```. See Help > Find externals > Preferences to find your exact paths.

2. Run Pure Data, and the shortcuts should now work!

### why not Purr Data?

[Purr Data](https://www.purrdata.net/), [PlugData](https://github.com/timothyschoen/PlugData), [Camomile](https://github.com/pierreguillot/Camomile) et al are wonderful forks that try to bring Pd into the 21th century. Unfortunately that means they use different rendering systems, so these tcl scripts won't apply to them. For now I'm using Pd vanilla, but if someone wants to replicate this work for one of the Pd forks, that would be super nice.