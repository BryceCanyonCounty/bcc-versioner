# BCC Anti Cheat
> A RedM standalone Github Version Checker API for your scripts!

## Features
- Resource Version Check export APIs
  - Github Release(tag) based check
  - Github Version file based check

## How to install
* Download this repo
* Copy and paste `bcc-versions` folder to `resources/bcc-versions`
* Add `ensure bcc-versions` to your `server.cfg` file
* Now you are ready to get coding!

## API Docs

### Version Check

This API will allow you to add a version check to your resource.

#### Release(Tag) Based Checks

_How to use [Github Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)_

> Create a Release and tag  with the version number

_Correct: `1.0.0`_

_Wrong: `v1.1.0`_

> Add the following contents to your lua server
```lua
local versioner = exports['bcc-versioner'].initiate()
local repo = 'https://github.com/BryceCanyonCounty/bcc-anticheat'
versioner.checkRelease(GetCurrentResourceName(), repo)
```

#### Version File Based Checks

> Create a file called `version` with the following contents
```txt
<1.3>
- More awesome updates
<1.1>
- Some awesome updates
<1.0>
- My first Update
```

> Add the following contents to your lua server
```lua
local versioner = exports['bcc-versioner'].initiate()
local repo = 'https://github.com/BryceCanyonCounty/bcc-anticheat'
versioner.checkFile(GetCurrentResourceName(), repo)
```

## Need More Support? 
- [Vorp Disord](https://discord.gg/DHGVAbCj7N)

## Requirements
- NONE! It's standalone.