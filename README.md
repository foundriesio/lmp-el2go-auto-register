# lmp-el2go-auto-register
A systemd oneshot helper to auto register a device using EdgeLock2GO

- This script should be the part of LmP based distro.
To configure it properly user should at least provide values for REPOID and root.crt
as described in the Foundries documentation:
https://docs.foundries.io/latest/user-guide/el2g.html#creating-an-lmp-build-with-edgelock-2go

- Files "default.env" and "root.crt" should be part of meta-subscriber-overrides layer.
They should replace empty files from meta-lmp layer.
Without these files generated images  will not contain FoundriesFactory specific values
and EdgeLock2GO registration will not work.
