<h1 align="center">
_Lib<br>

<a href="https://github.com/CreepyCre/_Lib"><img src="https://img.shields.io/badge/dynamic/json?color=informational&label=version&query=%24.version&url=https%3A%2F%2Fraw.githubusercontent.com%2FCreepyCre%2F_Lib%2Fmaster%2F_Lib%2Fscripts%2Ftools%2F_Lib.ddmod%3Fcallback%3D%3F" alt="Version"></a>
<a href="https://dungeondraft.net/"><img src="https://img.shields.io/badge/Dungeondraft-1.1.0.0%20Beta-blueviolet" alt="Dungeondraft version"></a>
<a href="https://github.com/CreepyCre/_Lib/blob/master/LICENSE"><img src="https://img.shields.io/github/license/CreepyCre/_Lib?color=900c3f" alt="License"></a>
</h1>

This mod offers additional API to simplify implementing certain features like configs and improve mod compatibility.

Current API:
- [ApiApi](https://github.com/CreepyCre/_Lib/wiki/ApiApi)
- [InputMapApi](https://github.com/CreepyCre/_Lib/wiki/InputMapApi)
- [ModConfigApi](https://github.com/CreepyCre/_Lib/wiki/ModConfigApi)
- [ModSignalingApi](https://github.com/CreepyCre/_Lib/wiki/ModSignalingApi)
- [PreferencesWindowApi](https://github.com/CreepyCre/_Lib/wiki/PreferencesWindowApi)

## Using _Lib
To be able to access _Lib's Api put the following at the top of your mods `start()` method:
```gdscript
Engine.emit_signal("_lib_register_mod", self)
```
Alternatively check if the signal exists first to ensure _Lib is actually enabled:
```gdscript
if not Engine.has_signal("_lib_register_mod"):
    return
Engine.emit_signal("_lib_register_mod", self)
```

After registering your mod with _Lib you will now have an entry `Global.API` available that contains all of the _Lib APIs. For more info on how to use them check out the [wiki](https://github.com/CreepyCre/_Lib/wiki).