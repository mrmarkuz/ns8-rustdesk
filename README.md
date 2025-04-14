# ns8-rustdesk

[RustDesk](https://rustdesk.com) is a full-featured open source remote control alternative for self-hosting and security with minimal configuration.

The [s6 image](https://github.com/rustdesk/rustdesk-server?tab=readme-ov-file#s6-overlay-based-images) is used in the app.

## Install

Install via Software center:

- Add a software repository pointing to https://repo.mrmarkuz.com/ns8/updates/
- Install RustDesk server via Software Center

Instantiate the module with:

    add-module ghcr.io/nethserver/rustdesk:latest 1

The output of the command will return the instance name.
Output example:

    {"module_id": "rustdesk1", "image_name": "rustdesk", "image_url": "ghcr.io/nethserver/rustdesk:latest"}

## Configure

Enter a FQDN to reach the RustDesk server.

### Client

Download a client from [RustDesk releases page](https://github.com/rustdesk/rustdesk/releases).

Get the public key on NS8:

    runagent -m rustdesk1 podman exec rustdesk-app cat id_ed25519.pub;echo

Enter your RustDesk server name or IP and the key:

![grafik](https://github.com/user-attachments/assets/a0fc7e0d-8f3d-4fc4-9776-f2f08715fdc2)

## Uninstall

To uninstall the instance:

    remove-module --no-preserve rustdesk1
