# samp-confirm-box

[![sampctl](https://img.shields.io/badge/sampctl-samp--confirm--box-2f2f2f.svg?style=for-the-badge)](https://github.com/GroWy/samp-confirm-box)

This library provides a simple [confirmation box](https://i.imgur.com/uyMuSAk.png) selectable or using keys, made using textdraws (better than dialogs).

## Installation

Simply install to your project:

```bash
sampctl package install GroWy/samp-confirm-box
```

Include in your code and begin using the library:

```pawn
#include <confirm-box>
```

## Usage

# Functions
```pawn
ShowPlayerConfirmBox(playerid, callback[], description[], title[], confirm_time, bool:selectable, bool:controllable, bool:sound);
```
Displays to the player the confirmation box.
```pawn
HidePlayerConfirmBox(playerid);
```
Hides the player's confirmation box.

# Definitions
`CONFIRMATION_BOX_TIME`: default value in milliseconds in how long the box will disappear.
`CONFIRM_BOX_UPDATE_RATE`: default update rate for the timer, how smaller is, how smooth is the bar effect (low values may impact your performance).<br>
`CONFIRMATION_BOX_ERROR`: default error code returned by confirm-box functions in case of fail.<br>

**Responses**:
`CONFIRM_BOX_RESPONSE_NULL`: when the player doesn't confirm or cancel the confirmation box.<br>
`CONFIRM_BOX_RESPONSE_YES`: when the player confirm the box.<br>
`CONFIRM_BOX_RESPONSE_NO`: when the player cancel the box.<br>

# Callbacks
You will make the callback, every confirm box will call a callback made by you using the below syntax:
```pawn
ConfirmBox:MyCallback(playerid, response, selectable, controllable, percent)
{
    // the parameters are optional, depending on what you need.
    // here will be your code.
    return 1;
}
```

## Testing

To test, simply run the package:

```bash
sampctl package run
```
