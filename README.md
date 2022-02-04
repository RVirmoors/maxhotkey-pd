# maxhotkey-pd
 Pure Data plugin implementing Max-like key&mouse shortcuts & UI behaviour.

 Tested on Pd vanilla 0.52 win x64. 
 
 Made possible by [Monetus](https://github.com/monetus), [Seb Shader](https://github.com/sebshader) and others on the [Pd forum](https://forum.pdpatchrepo.info/topic/13810/a-gui-plugin-adding-max-hotkeys-and-ui-feel-to-pd-vanilla).

## included

| command | action | done |
|---------|--------|------|
| ctrl+click on canvas | toggle edit mode | ✅ | 
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
| enter | apply object | ✅ |
| alt+drag | duplicate | ❌ |
| ctrl+shift+Y | arrange | ❌ |

(replace ctrl with cmd and alt with option for OSX)

I started this as a complete tcl/tk newbie, so the hard stuff (❌) will take a while to implement. Any contributions are welcome!

All the key bindings (including some not present in Max) are under the `set keybindings` line in `maxhotkey.cfg`. Feel free to modify them to suit your needs.

## installing

1. Download and copy `maxhotkey-plugin.tcl` to a folder in Pd's path, like ```Documents/Pd/externals```. See Help > Find externals > Preferences to find your exact paths.

2. Run Pure Data, and the shortcuts should now work!

---

### why not Purr Data?

[Purr Data](https://www.purrdata.net/), [Pd-L2Ork](https://puredata.info/downloads/Pd-L2Ork), [PlugData](https://github.com/timothyschoen/PlugData), [Camomile](https://github.com/pierreguillot/Camomile) et al are wonderful forks that bring Pd into the 21th century. Unfortunately that means they use different rendering systems, so these tcl scripts won't apply to them. For now I'm focussing on Pd vanilla, but if someone wants to replicate this work for one of the Pd forks, that would be super nice.

### known issues

Adding the [PD AutoComplete Plugin](https://github.com/HenriAugusto/completion-plugin) breaks these hotkeys. For now, a quick fix is to add 
```tcl
pdtk_text_editing_old $mytoplevel $tag $editing
``` 
at the end of the `pdtk_text_editing` proc in [completion-plugin.tcl](https://github.com/HenriAugusto/completion-plugin/blob/master/completion-plugin.tcl) (line 691)
