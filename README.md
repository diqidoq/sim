# sim
Simple desktop screenshot command based on import and imagemagick

## Installation

    mkdir -p ~/share && cd ~/share
    git clone https://github.com/diqidoq/sim.git
    sudo chmod a+x sim/sim
    sudo ln -s ~/share/sim/sim /usr/local/bin/sim
    sudo chmod a+x /usr/local/bin/sim
    
Now simply type sim to make a screenshot of your whole desktop

## How to implement with Debian (and LXDE PrintScreen keybind)

Open the LXDE config file near line ~ 320-350.

    sudo vim ~/.config/openbox/lxde-rc.xml
    
Add (or replace if exist) this group into the keybind section of the config file.

    <!-- Launch screenshot when PrintScreen is pressed -->
    <keybind key="Print">
      <action name="Execute">
        <command>sim</command>
      </action>
    </keybind>

