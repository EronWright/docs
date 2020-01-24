---
title: AliCloud Setup
meta_desc: This page provides an overview on how to configure credentials for the Pulumi AliCloud Provider.
---

The [Pulumi AliCloud provider]({{< relref "./" >}}) uses the AliCloud SDK to manage and provision resources.

> Pulumi relies on the AliCloud SDK to authenticate requests from your computer to AliCloud. Your credentials are never sent
> to pulumi.com.

The [Pulumi AliCloud Provider]({{< relref "./" >}}) needs to be configured with AliCloud credentials
before it can be used to create resources.

### Configuring Credentials

Once obtained, there are two ways to communicate your authorization tokens to Pulumi:

1. Set the environment variables `ALICLOUD_ACCESS_KEY` and `ALICLOUD_SECRET_KEY`:

    ```bash
    $ export ALICLOUD_ACCESS_KEY=XXXXXXXXXXXXXX
    $ export ALICLOUD_SECRET_KEY=YYYYYYYYYYYYYY
    ```

2. Set them using configuration, if you prefer that they be stored alongside your Pulumi stack for easy multi-user access:

    ```bash
    $ pulumi config set alicloud:accessKey XXXXXXXXXXXXXX --secret
    $ pulumi config set alicloud:secretKey YYYYYYYYYYYYYY --secret
    ```

Remember to pass `--secret` when setting `alicloud:secretKey` and `alicloud:accessKe` so that they are properly encrypted.
A full set of configuration parameters can be found listed on the [Project README](https://github.com/pulumi/pulumi-alicloud/blob/master/README.md).
