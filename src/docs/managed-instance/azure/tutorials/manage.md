# Manage Stateful Nodes

Elastigroup enables you to see an overview of all your stateful nodes, get status at a glance, perform tasks such as importing and creating new stateful nodes, and drill down to more detailed information when you need to.

To manage your stateful nodes in the Spot console, go to Elastigroup in the menu tree and click Stateful Nodes.

<img src="/elastigroup/_media/azure-manage-stateful-nodes-01b.png" />

## View List of Stateful Nodes

The list of stateful nodes gives you a quick view of your nodes and basic information including:
- Node Name: The user-given name of the node.
- ID: The unique identifier that Elastigroup assigned to the node upon creation.
- VM Name: The Azure VM name. Click the VM Name to load the Azure portal for this specific VM.
- Region: The Azure region where the node is located.
- Availability Zone: The Azure availability zone where the VM is located.
- VM Size: The VM size assigned to the node.
- Life Cycle: Spot or on-demand.
- Public IP: The public IP address which is assigned to the VM.
- Private IP: The private IP address which is assigned to the VM.
- Creation Date: The date the node was created.
- Status: The activity status of the node (e.g., Running, Paused).

## Filter Node List

If you have a long list of stateful nodes, you can use the filter above the list to find one or multiple nodes. Just enter a tag, a node attribute, a keyword or simply a string of text into the filter box and type enter.

<img src="/elastigroup/_media/azure-manage-stateful-nodes-02.png" />

## View Node Details

To get detailed information, statistics, and operational information about a stateful node, click on the Node Name. This will open the Node Details page for that node which serves as your operational dashboard for the node.

## Create Node

You can do the following from the dropdown menu:

* Create a new node from scratch.
* Import an existing VM from Azure.  

<img src="/elastigroup/_media/azure-manage-stateful-edit-5.png" width="300"/>

## Use Node Actions

To perform one of the [node actions](managed-instance/azure/features/actions), click on the Actions menu on the top right and click one of the actions. The actions available include:
- View Configuration
- Recycle
- Pause
- Resume
- Delete

<img src="/elastigroup/_media/azure-manage-stateful-edit-6.png" />

## Edit Node Configuration

When the node status is either Running or Paused, you can edit the node’s configuration in the creation wizard.  

Hover over the relevant row of the node you want to configure in the table and click the Edit icon that appears on the right.

<img src="/elastigroup/_media/azure-manage-stateful-edit-1.png" />

If you are on the Overview page, click Edit Node at the top right.

<img src="/elastigroup/_media/azure-manage-stateful-edit-2.png" />

You can then edit any of the fields in the Basics page that appear.

<img src="/elastigroup/_media/azure-manage-stateful-edit-3.png" />

You can also go to the Review page and edit directly in the JSON configuration. In the Review page, do the following:

1. Click JSON and click Edit Mode.  

<img src="/elastigroup/_media/azure-manage-stateful-edit-4.png" />

2. Make your changes in the JSON configuration and click Update.

Your changes to the configuration are saved and applied to the stateful node. Changes that affect the VM directly (e.g., selected availability zones or VM sizes) will be reflected only when the next VM is launched. In order to make the changes take effect immediately, a [Recycle](managed-instance/azure/features/actions?id=recycle) action is required on the stateful node.

The following parameters cannot be edited and are not included in the JSON configuration that is editable:

`id`<br>
`region`<br>
`resourceGroupName`<br>
`compute.os`

> Tip: You can edit a node only when it is in Running or Paused state.

## What’s Next?

Learn more about the [Stateful Node Details](managed-instance/azure/tutorials/view-details) view.
