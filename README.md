# sim
Simple desktop screenshot command based on import and imagemagick for Debian like Linux OS.

## Installation

Open your terminal and run following bash commands.

    sudo apt-get update && sudo apt-get install vim imagemagick -y
    mkdir -p ~/share && cd ~/share
    git clone https://github.com/diqidoq/sim.git
    sudo chmod a+x sim/sim
    sudo ln -s ~/share/sim/sim /usr/local/bin/sim
    sudo chmod a+x /usr/local/bin/sim
    
Now simply type `sim` to make a screenshot of your whole desktop screen session.

### How to implement in openbox/LXDE PrintScreen keybind under Debian

Open the LXDE config file near line ~ 320-350 or near the "Print" keybind group if exist.

    sudo vim +320 ~/.config/openbox/lxde-rc.xml

or

    sudo vim +/key=\"Print\" ~/.config/openbox/lxde-rc.xml

Add (or replace if exist) the following "Print" group into the keybind section of the config file.

    <!-- Launch screenshot when PrintScreen is pressed -->
    <keybind key="Print">
      <action name="Execute">
        <command>sim</command>
      </action>
    </keybind>

Save (:wq!) and restart openbox/LXDE with following terminal command:

    openbox --reconfigure
