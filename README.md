# ns8-rustdesk

[RustDesk](https://rustdesk.com) is a full-featured open source remote control alternative for self-hosting and security with minimal configuration.

## Install

Instantiate the module with:

    add-module ghcr.io/nethserver/rustdesk:latest 1

The output of the command will return the instance name.
Output example:

    {"module_id": "rustdesk1", "image_name": "rustdesk", "image_url": "ghcr.io/nethserver/rustdesk:latest"}

## Configure

Enter a FQDN to reach the Rustdesk server.

## Uninstall

To uninstall the instance:

    remove-module --no-preserve rustdesk1

