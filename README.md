# Minimal Emacs key bindings for Karabiner-Elements

![karabiner-preferences](https://user-images.githubusercontent.com/1632335/116778108-fb2b1900-aaaa-11eb-908d-7e5008cd6319.png)

A minimal Emacs key bindings for [Karabiner-Elements](https://karabiner-elements.pqrs.org/). You can enable/disable each of key bindings so that keep influences minimal to original applications.

This key bindings is based on [Emacs key bindings (rev 12)](https://github.com/pqrs-org/KE-complex_modifications/blob/master/src/json/emacs_key_bindings.json.rb) by [@tekezo](https://github.com/tekezo).

## Install

- Copy `minimal_emacs.json`

```sh
% git clone https://github.com/susumuota/karabiner_minimal_emacs
% cd karabiner_emacs_minimal
% cp emacs_minimal.json ~/.config/karabiner/assets/complex_modifications/
```

- Open `Preferences...`
- Click `Complex modifications`. See details [here](https://karabiner-elements.pqrs.org/docs/manual/configuration/configure-complex-modifications/).
- Click `Add rule`
- Expand `Minimal Emacs key bindings`
- Click `Enable All` or Click `Enable` for specific key bindings

## Extend

At the moment this key bindings only apply to Microsoft Excel, PowerPoint and Word. However you can easily extend them by editing `"conditions"` like the following, e.g. `"^com\\.google\\.Chrome$"`. See details [here](https://karabiner-elements.pqrs.org/docs/json/complex-modifications-manipulator-definition/conditions/frontmost-application/).

```json
          "conditions": [
            {
              "type": "frontmost_application_if",
              "bundle_identifiers": [
                "^com\\.microsoft\\.Excel$",
                "^com\\.microsoft\\.Powerpoint$",
                "^com\\.microsoft\\.Word$",
                "^com\\.google\\.Chrome$"
              ]
            }
          ]
```

## Author

Susumu OTA

https://github.com/susumuota