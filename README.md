# IgiLoad
IgiLoad script - logistical support

## Original Information:
**Developed by**: [igi_pl](http://www.igipl.net/en/)

**Documentation at**: [igipl.net](http://www.igipl.net/en/arma3/igiload-script) and [forums.bohemia.net](https://forums.bohemia.net/forums/topic/163358-igiload-script-logistical-support/)

```
The main task for IgiLoad script is to allow delivery of supplies to units away
from base. In short, transport boxes with ammunition, weapons, or anything else
(what you put in the box) using vehicles.
```

## Project Information:
This is an attempt to do the following
* Fix cargo clipping issues for various vehicle types
* Optimize the code for performance
  * Attempt to refactor the code for easier modification
  * Improve documentation of functionality for future modders
* Seperate the current vehicle groups into more intuitive categories
  * Allow for finer control of different animations, cargo amounts, and cargo positions
* Support vehicles from both ARMA expansions and a few select mods

*Disclaimer*: I have no idea what I'm doing.

## Changelog:

### 0.1

#### `IgiLoad\IgiLoad.sqf`
* `APC` load mechanic support added across the board. From interface to loading animation.
  * Added all variants from base game, expansions, CUP, and Exiles.
  * Cargohold size is `2` containers; limited to `IL_Supported_Box_H1` and `IL_Supported_Box_H2`
* `Dingo` load mechanic support added across the board. From interface to loading animation.
  * Added all variants from CUP.
  * Cargohold size is `1` containers; limited to `IL_Supported_Box_H1` and `IL_Supported_Box_H2`
* `KAMAZ` section entirely rewritten to only include `Zamak` vehicles.
  * Added all variants from base game, expansions, and Exile.
  * Fixed CAPITAL LETTERS on interface.
  * Fixed forward axis clipping issues.
  * Vehicle to Vehicle support for loading this type into other vehicles added. Premature feature, unused.
* `HMMWV` load mechanic support added across the board. From interface to loading animation.
  * Added all variants from base game, expansions, CUP, and Exile.
  * Cargohold size is `1` containers; limited to `IL_Supported_Box_H1` and `IL_Supported_Box_H2`
  * Vehicle to Vehicle support for loading this type into other vehicles added. Premature feature, unreliable.
* `Ural` section improvements
  * Added all variants from base game, expansions, CUP, and Exile.
  * Cargohold size reduced to `3` containers, down from `4`, preventing clipping issues
  * Fixed forward axis clipping issues.
* Configuration changes
  * `IL_SDistL` increased to `4`, up from `2.5`, to extend cargo gathering radius. Wonky hitbox workaround.