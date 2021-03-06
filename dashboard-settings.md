---

Copyright:
  years: 2016,2020
lastupdated: "2020-12-07"

keywords: elasticsearch, compose

subcollection: ComposeForElasticsearch

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}

# Settings
{: #dashboard-settings}

Use these features to adapt your {{site.data.keyword.composeForElasticsearch_full}} service to suit your needs and requirements.

## Upgrade Version

If a new version of the database is available, a drop-down menu appears, which you can use to select the version you want to upgrade to. Otherwise, your service is on the newest version available, and the pane displays the current version information.

![The Version pane](./images/elastic_search-version-show.png "The Version pane")

## Scale Resources

You can increase or reduce the amount of storage that is allocated to your service by scaling resources.

1. Navigate to your service's dashboard overview page.
2. In the _Deployment Details_ pane, click **Scale Resources**. The Scale Resources page opens.
    ![The Scale Resources page](./images/elastic_search-scale-show.png "The Scale Resources page")
3. Adjust the slider to increase or reduce the storage that is allocated to the {{site.data.keyword.composeForElasticsearch}} service. Move the slider to the left to reduce the amount of storage, or move it to the right to increase the storage.
4. Click **Scale Deployment** to trigger the rescaling and return to the dashboard overview. 

When the scaling is complete the _Deployment Details_ pane updates to show the current usage and the new value for the available storage.


## Using allowlists

If you want to restrict access to your databases, you can allowlist specific IP addresses or ranges of IP addresses on your service. When there are no IP addresses in the allowlist, the allowlist is disabled and the deployment accepts connections from any system on the internet.

![Allowlisting IP addresses](./images/elastic_search-allowlist-show.png "The allowlist fields.")

### IP addresses
The *IP* field can take a single complete IPv4 address or IPv6 address with or without a netmask. Without a netmask, incoming connections must come from exactly that IP address. 

Although the IP entry allows for IPv6, no Compose deployments are currently available to IPv6 networking and so these addresses cannot be filtered on.
{: tip}

### Netmasks
To allow a connection from a specified range of IP addresses, use a netmask. The IP address must be fully specified. That means entering, for example, `192.168.1.0/24` rather than `192.168.1/24`.

### Description
The *Description* can be any user-significant text for identifying the allowlist entry - a customer name, project identifier, or employee number, for example. The description field is required.

### Compose Services
Allowlist entries are automatically added to Compose's servers to allow them to connect.

### Removal
To remove an IP address or netmask from the allowlist, click the *Remove* entry displayed next to it.
When all entries on the allowlist are removed, the allowlist is disabled and all IP addresses are accepted by the TCP access portals.
