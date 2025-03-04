---
repository: "https://github.com/turbot/steampipe-mod-azure-thrifty"
---

# Azure Thrifty Mod

Be Thrifty on Azure! This mod checks for unused resources and opportunities to optimize your spend on Azure.

![image](https://raw.githubusercontent.com/turbot/steampipe-mod-azure-thrifty/main/docs/azure-thrifty-console-graphic.png)

## References

[Azure](https://azure.microsoft.com) provides on-demand cloud computing platforms and APIs to authenticated customers on a metered pay-as-you-go basis.

[Steampipe](https://steampipe.io) is an open source CLI to instantly query cloud APIs using SQL.

[Steampipe Mods](https://steampipe.io/docs/reference/mod-resources#mod) are collections of `named queries`, and codified `controls` that can be used to test current configuration of your cloud resources against a desired configuration.

## Documentation

- **[Benchmarks and controls →](https://hub.steampipe.io/mods/turbot/azure_thrifty/controls)**
- **[Named queries →](https://hub.steampipe.io/mods/turbot/azure_thrifty/queries)**

## Get started

Install the Azure plugin with [Steampipe](https://steampipe.io):

```shell
steampipe plugin install azure
```

Clone:

```sh
git clone https://github.com/turbot/steampipe-mod-azure-thrifty.git
cd steampipe-mod-azure-thrifty
```

Run all benchmarks:

```shell
steampipe check all
```

Run a specific control:

```shell
steampipe check control.compute_disk_unattached
```

### Credentials

This mod uses the credentials configured in the [Steampipe Azure plugin](https://hub.steampipe.io/plugins/turbot/azure).

### Configuration

Several benchmarks have [input variables](https://steampipe.io/docs/using-steampipe/mod-variables) that can be configured to better match your environment and requirements. Each variable has a default defined in `steampipe.spvars`, but these can be overwritten in several ways:

- Modify the `steampipe.spvars` file
- Remove or comment out the value in `steampipe.spvars`, after which Steampipe will prompt you for a value when running a query or check
- Pass in a value on the command line:

  ```shell
  steampipe check benchmark.compute --var=compute_disk_max_size_gb=100
  ```

- Set an environment variable:

  ```shell
  compute_disk_max_size_gb=100 steampipe check control.compute_disk_large
  ```

  - Note: When using environment variables, if the variable is defined in `steampipe.spvars` or passed in through the command line, either of those will take precedence over the environment variable value. For more information on variable definition precedence, please see the link below.

These are only some of the ways you can set variables. For a full list, please see [Passing Input Variables](https://steampipe.io/docs/using-steampipe/mod-variables#passing-input-variables).

## Get involved

- Contribute: [Help wanted issues](https://github.com/turbot/steampipe-mod-azure-thrifty/labels/help%20wanted)
- Community: [Slack channel](https://join.slack.com/t/steampipe/shared_invite/zt-oij778tv-lYyRTWOTMQYBVAbtPSWs3g)
