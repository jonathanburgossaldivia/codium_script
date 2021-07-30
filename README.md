# codium_script
Solve the problem "Cannot connect to Extensions marketplace" on Open Suse

Run this command:

sudo sed -i 's/--unity-launch %F/add --disable-web-security/;s/--new-window %F/add --disable-web-security/' /usr/share/applications/codium.desktop
