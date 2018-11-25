<h1 align="center">Roact (TypeScript)</h1>
<div align="center">
	<a href="https://travis-ci.org/Roblox/roact">
		<img src="https://api.travis-ci.org/Roblox/roact.svg?branch=master" alt="Travis-CI Build Status" />
	</a>
	<a href="https://coveralls.io/github/Roblox/roact?branch=master">
		<img src="https://coveralls.io/repos/github/Roblox/roact/badge.svg?branch=master" alt="Coveralls Coverage" />
	</a>
	<a href="https://roblox.github.io/roact">
		<img src="https://img.shields.io/badge/docs-website-green.svg" alt="Documentation" />
	</a>
</div>

<div align="center">
	A declarative UI library for Roblox Lua inspired by <a href="https://reactjs.org">React</a>.
</div>

<div>&nbsp;</div>

## Installation

At the moment rbx-roact is source only. It will be available as a package soon&trade;

## Usage
For a detailed guide and examples, check out [the official Roact documentation](https://roblox.github.io/roact). The Wiki on this repository will have guides on how to adapt to using typescript instead of Lua.

```typescript
import * as Roact from 'rbx-roact';

const LocalPlayer = game.GetService("Players").LocalPlayer as Player;
const PlayerGui = LocalPlayer.FindFirstChildOfClass("PlayerGui");

const tree = Roact.createElement("ScreenGui", {}, {
  Label: Roact.createElement("TextLabel", {
    Text: "Hello, World!",
    Size: new UDim2(1, 0, 1, 0)
  });
});

Roact.mount(tree, PlayerGui, "HelloWorld");
```


## Future

in the future, this will also be acceptable usage

```tsx
import * as Roact from 'rbx-roact';

const LocalPlayer = game.GetService("Players").LocalPlayer as Player;
const PlayerGui = LocalPlayer.FindFirstChildOfClass("PlayerGui");

const tree = <rbxScreenGui>
  <rbxTextLabel key="Label" Text="Hello, World!" Size={new UDim2(1, 0, 1, 0)}/>
</rbxScreenGui>;

Roact.mount(tree, PlayerGui, "HelloWorld");
```

## License
The original Roact library's License can be found here: [Roact License](https://github.com/Roblox/roact/blob/master/LICENSE)
