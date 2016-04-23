# sim
screenshot command based on import and imagemagick

## How to implement with Debian LXDE PrintScreen keybind

Open the LXDE config file near line ~ 320-350.

    sudo vim ~/.config/openbox/lxde-rc.xml
    
Add this group into the keybind section of the config file.

    <!-- Launch screenshot when PrintScreen is pressed -->
    <keybind key="Print">
      <action name="Execute">
        <command>sim</command>
      </action>
    </keybind>
    <!-- Launch LXRandR when Fn+Screen is pressed -->
    <keybind key="XF86Display">
      <action name="Execute">
        <command>lxrandr</command>
      </action>
    </keybind>
