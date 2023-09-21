# Rancher Turtles - Fleet Example

This repository can be used to import clusters into Rancher using Fleet. There are a number of different branches that you can use that demonstrate different aspects of this integration:

- **[main](https://github.com/rancher-sandbox/rancher-turtles-fleet-example/tree/main)** - used for importing cluster definitions where all clusters within a namespace are automatically imported into Rancher.
- **per-cluster-import (this branch)** - used for importing cluster definitions where individual clusters are marked for auto-importing into Rancher.
- **[templates](https://github.com/rancher-sandbox/rancher-turtles-fleet-example/tree/templates)** - contains Cluster API templates that are used by the Rancher Turtles documentation.

Switch to the branch to read further information.

## Branch explanation

The [clusters](./clusters/) folder contains the definition for the clusters that you want to create and have imported into Rancher Manager. These definitions can be created using **clusterctl** or hand crafted. See the [Rancher Turtles documentation](https://rancher-sandbox.github.io/rancher-turtles-docs/) for further details.

The [fleet.yaml](fleet.yaml) file contains configuration used by Fleet when creating bundles. Specifically in this file we are declaring that the cluster definitions should be placed in a namespace called **default**.

The cluster definition in [cluster1.yaml](./clusters/cluster1.yaml) is labled so that it is auto-imported into Rancehr when it is Ready. See the **Cluster** kind in the file.
