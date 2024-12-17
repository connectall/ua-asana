
# ua-asana

The ConnectALL Asana Universal Adapter is developed as an extension to the universal adapter capability of ConnectALL. This adapter will allow the user to use Asana with ConnectALL. Current capabilities and limitations will be defined below.

Please refer to the [ConnectALL Tech Docs](https://techdocs.broadcom.com/us/en/ca-enterprise-software/valueops/connectall/3-6/adapters/universal-adapter.html) for more information on the ConnectALL Universal Adapter.

If you are an existing SaaS customer, please contact Broadcom Support to enable the adapter in your environment. If you are using ConnectALL On-Premise, you may download and install this adapter in your environment. If you are not yet a customer, [please reach out to learn more](https://enterprise-software.broadcom.com/contact-us).

# Setup

## Supported Entities

This Universal Adapter currently supports the following entities:
* Projects
* Tasks

*Note: This Universal Adapter is provided as-is. It is tested and validated using the entities and configurations as defined. Any additional customizations are not supported and should be made at your own discretion.*

## Connection Details
Authentication to Asana is supported using personal access tokens (PATs) or Service Accounts (SAs). See the [Asana API Authenticaiton](https://developers.asana.com/docs/authentication) documentation for more info.
* **Connection Name:** *Name of Application*
* **Application Type:** *asana*
* **URL:** *Base URL for application API (ex: https://app.asana.com)*
* **User Name:** *Not Used, leave blank*
* **Password:** *Not Used, leave blank*
* **Application Category:** *Select from dropdown list*
* **Time Zone:** *Not Required*
* **Select Group:** *Select Group if neccessary*
* **Auth Option:** *Header*
* **Authentication Type:** *ApiKey*
* **API Key:** *Authorization*
* **API Value:** *Bearer <your_PAT_or_SA_goes_here>*

## Flow Filters

Optional filter of projects by workspace or team.

workspace=1331

team=11496


## Example Automation

*Sync Projects and Tasks in Clarity to Projects and Tasks in Asana.*

# Known Limitations

* An Asana Task is supported only under a single Project. A single Task assigned to multiple Projects is typically not supported by other tools and is not supported in this version of the adapter.
* The Status and Priority fields have been defined with sample gids. These values will need to be changed to match the custom field gids of the target Asana workspace. Additional custom fields with thier gids can be added to the Fields list.


# How to use
## Import specifications
* Import asana_config.zip into ConnectALL using "Install custom adapter" feature.
## Define application links
* Create an application link in ConnectALL between Asana and another application of your choice.
* Navigate to `Configuration -> Connections` screen and create a new connection to Asana.
* In the Entity mapping tab under Advanced Properties choose "Sync Type" as POLL
* In the field mapping tab add the field that you want to sync between the applications.


# Supporting Documentation

Third Party API Documentation: [Asana API Documentation](https://developers.asana.com/reference/rest-api-reference)
