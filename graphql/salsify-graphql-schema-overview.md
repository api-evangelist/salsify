---
updatedAt: 2026-05-19T13:41:04.000Z
---

Fetch the complete documentation index at: https://developers.salsify.com/llms.txt. Use this file to discover all available pages before exploring further.

# GraphQL Schema Overview

# Schema Types

<details>
  <summary><strong>Table of Contents</strong></summary>

\- [Query](#query)

* [Mutation](#mutation)
* [Objects](#objects)
  * [Account](#account)
  * [AccountOrganization](#accountorganization)
  * [AccountOrganizationPaginatedList](#accountorganizationpaginatedlist)
  * [AccountPaginatedList](#accountpaginatedlist)
  * [CanceledProvisionOrganizationRequest](#canceledprovisionorganizationrequest)
  * [CompletedConfigurationManifestEntityTypeInstallation](#completedconfigurationmanifestentitytypeinstallation)
  * [CompletedConfigurationManifestEntityTypeVersionRequest](#completedconfigurationmanifestentitytypeversionrequest)
  * [CompletedConfigurationManifestInstallation](#completedconfigurationmanifestinstallation)
  * [CompletedConfigurationManifestVersionRequest](#completedconfigurationmanifestversionrequest)
  * [CompletedProvisionOrganizationRequest](#completedprovisionorganizationrequest)
  * [ConfigurationManifest](#configurationmanifest)
  * [ConfigurationManifestEntityType](#configurationmanifestentitytype)
  * [ConfigurationManifestEntityTypeVersion](#configurationmanifestentitytypeversion)
  * [ConfigurationManifestInstallationPaginatedList](#configurationmanifestinstallationpaginatedlist)
  * [ConfigurationManifestPaginatedList](#configurationmanifestpaginatedlist)
  * [ConfigurationManifestVersion](#configurationmanifestversion)
  * [ConfigurationManifestVersionPaginatedList](#configurationmanifestversionpaginatedlist)
  * [ConfigurationManifestVersionRequestPaginatedList](#configurationmanifestversionrequestpaginatedlist)
  * [CreateConfigurationManifestFromFilePayload](#createconfigurationmanifestfromfilepayload)
  * [CreateConfigurationManifestFromOrganizationPayload](#createconfigurationmanifestfromorganizationpayload)
  * [CreateConfigurationManifestVersionFromFilePayload](#createconfigurationmanifestversionfromfilepayload)
  * [CreateConfigurationManifestVersionFromOrganizationPayload](#createconfigurationmanifestversionfromorganizationpayload)
  * [DeleteAccountSandboxOrganizationPayload](#deleteaccountsandboxorganizationpayload)
  * [DeleteConfigurationManifestPayload](#deleteconfigurationmanifestpayload)
  * [FailedConfigurationManifestEntityTypeInstallation](#failedconfigurationmanifestentitytypeinstallation)
  * [FailedConfigurationManifestEntityTypeVersionRequest](#failedconfigurationmanifestentitytypeversionrequest)
  * [FailedConfigurationManifestInstallation](#failedconfigurationmanifestinstallation)
  * [FailedConfigurationManifestVersionRequest](#failedconfigurationmanifestversionrequest)
  * [FailedProvisionOrganizationRequest](#failedprovisionorganizationrequest)
  * [InstallConfigurationManifestPayload](#installconfigurationmanifestpayload)
  * [InstantiateWorkflowPayload](#instantiateworkflowpayload)
  * [Organization](#organization)
  * [OrganizationPaginatedList](#organizationpaginatedlist)
  * [PageMetadata](#pagemetadata)
  * [PreviewConfigurationManifestPayload](#previewconfigurationmanifestpayload)
  * [ProvisionOrganizationPayload](#provisionorganizationpayload)
  * [RenderConfigurationManifestPayload](#renderconfigurationmanifestpayload)
  * [RunningConfigurationManifestEntityTypeInstallation](#runningconfigurationmanifestentitytypeinstallation)
  * [RunningConfigurationManifestEntityTypeVersionRequest](#runningconfigurationmanifestentitytypeversionrequest)
  * [RunningConfigurationManifestInstallation](#runningconfigurationmanifestinstallation)
  * [RunningConfigurationManifestVersionRequest](#runningconfigurationmanifestversionrequest)
  * [RunningProvisionOrganizationRequest](#runningprovisionorganizationrequest)
  * [StoppedConfigurationManifestEntityTypeInstallation](#stoppedconfigurationmanifestentitytypeinstallation)
  * [StoppedConfigurationManifestInstallation](#stoppedconfigurationmanifestinstallation)
  * [User](#user)
  * [WorkflowInstance](#workflowinstance)
* [Inputs](#inputs)
  * [ConfigurationManifestFileSourceInput](#configurationmanifestfilesourceinput)
  * [ConfigurationManifestInstallationEntityTypeSelectionInput](#configurationmanifestinstallationentitytypeselectioninput)
  * [ConfigurationManifestInstallationFilterFieldReferenceInput](#configurationmanifestinstallationfilterfieldreferenceinput)
  * [ConfigurationManifestInstallationFilterInput](#configurationmanifestinstallationfilterinput)
  * [ConfigurationManifestInstallationFilterMultivaluedComparisonInput](#configurationmanifestinstallationfiltermultivaluedcomparisoninput)
  * [ConfigurationManifestInstallationFilterValueInput](#configurationmanifestinstallationfiltervalueinput)
  * [CreateConfigurationManifestFromFileInput](#createconfigurationmanifestfromfileinput)
  * [CreateConfigurationManifestFromOrganizationInput](#createconfigurationmanifestfromorganizationinput)
  * [CreateConfigurationManifestVersionFromFileInput](#createconfigurationmanifestversionfromfileinput)
  * [CreateConfigurationManifestVersionFromOrganizationInput](#createconfigurationmanifestversionfromorganizationinput)
  * [DeleteAccountSandboxOrganizationInput](#deleteaccountsandboxorganizationinput)
  * [DeleteConfigurationManifestInput](#deleteconfigurationmanifestinput)
  * [FilterNowInput](#filternowinput)
  * [FilterRelativeTimeInput](#filterrelativetimeinput)
  * [FilterSearchInput](#filtersearchinput)
  * [InstallConfigurationManifestInput](#installconfigurationmanifestinput)
  * [InstantiateWorkflowInput](#instantiateworkflowinput)
  * [PaginationInput](#paginationinput)
  * [PreviewConfigurationManifestInput](#previewconfigurationmanifestinput)
  * [ProvisionOrganizationInput](#provisionorganizationinput)
  * [RenderConfigurationManifestInput](#renderconfigurationmanifestinput)
  * [WorkflowEntityInput](#workflowentityinput)
* [Enums](#enums)
  * [AccountType](#accounttype)
  * [ConfigurationManifestEntityTypeValue](#configurationmanifestentitytypevalue)
  * [ConfigurationManifestInstallationFilterField](#configurationmanifestinstallationfilterfield)
  * [PaginationInputType](#paginationinputtype)
  * [WorkflowEntityType](#workflowentitytype)
* [Scalars](#scalars)
  * [Boolean](#boolean)
  * [ConfigurationManifestYaml](#configurationmanifestyaml)
  * [ID](#id)
  * [Identifier](#identifier)
  * [Int](#int)
  * [Iso8601DateTime](#iso8601datetime)
  * [Json](#json)
  * [String](#string)
  * [Url](#url)
* [Interfaces](#interfaces)
  * [ConfigurationManifestEntityTypeInstallation](#configurationmanifestentitytypeinstallation)
  * [ConfigurationManifestEntityTypeVersionRequest](#configurationmanifestentitytypeversionrequest)
  * [ConfigurationManifestInstallation](#configurationmanifestinstallation)
  * [ConfigurationManifestVersionRequest](#configurationmanifestversionrequest)
  * [ProvisionOrganizationRequest](#provisionorganizationrequest)

</details>

## Query

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>account</strong></td>
<td valign="top"><a href="#account">Account</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accounts</strong></td>
<td valign="top"><a href="#accountpaginatedlist">AccountPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizations</strong></td>
<td valign="top"><a href="#organizationpaginatedlist">OrganizationPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>provisionOrganizationRequest</strong></td>
<td valign="top"><a href="#provisionorganizationrequest">ProvisionOrganizationRequest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createConfigurationManifestFromFile</strong></td>
<td valign="top"><a href="#createconfigurationmanifestfromfilepayload">CreateConfigurationManifestFromFilePayload</a></td>
<td>

Creates a new configuration manifest in the specified account from a given YAML source and begins creating the first version of the manifest

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createconfigurationmanifestfromfileinput">CreateConfigurationManifestFromFileInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createConfigurationManifestFromOrganization</strong></td>
<td valign="top"><a href="#createconfigurationmanifestfromorganizationpayload">CreateConfigurationManifestFromOrganizationPayload</a></td>
<td>

Creates a new configuration manifest in the specified account from a given organization and begins creating the first version of the manifest

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createconfigurationmanifestfromorganizationinput">CreateConfigurationManifestFromOrganizationInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createConfigurationManifestVersionFromFile</strong></td>
<td valign="top"><a href="#createconfigurationmanifestversionfromfilepayload">CreateConfigurationManifestVersionFromFilePayload</a></td>
<td>

Creates new version of given filed-based manifest in specified account from the given YAML source

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createconfigurationmanifestversionfromfileinput">CreateConfigurationManifestVersionFromFileInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createConfigurationManifestVersionFromOrganization</strong></td>
<td valign="top"><a href="#createconfigurationmanifestversionfromorganizationpayload">CreateConfigurationManifestVersionFromOrganizationPayload</a></td>
<td>

Creates new version of given organization-based manifest in specified account from the manifest's source organization

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#createconfigurationmanifestversionfromorganizationinput">CreateConfigurationManifestVersionFromOrganizationInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteConfigurationManifest</strong></td>
<td valign="top"><a href="#deleteconfigurationmanifestpayload">DeleteConfigurationManifestPayload</a></td>
<td>

Deletes the specified manifest in the given account

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteconfigurationmanifestinput">DeleteConfigurationManifestInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>installConfigurationManifest</strong></td>
<td valign="top"><a href="#installconfigurationmanifestpayload">InstallConfigurationManifestPayload</a></td>
<td>

Installs the given manifest in the provided organization, with the inputs injected at installation time (if the manifest is parameterized)

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#installconfigurationmanifestinput">InstallConfigurationManifestInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>previewConfigurationManifest</strong></td>
<td valign="top"><a href="#previewconfigurationmanifestpayload">PreviewConfigurationManifestPayload</a></td>
<td>

Renders the given manifest and returns the result, with the inputs injected into the manifest. Primarily used to preview persisted manifests before installation into an organization

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#previewconfigurationmanifestinput">PreviewConfigurationManifestInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>renderConfigurationManifest</strong></td>
<td valign="top"><a href="#renderconfigurationmanifestpayload">RenderConfigurationManifestPayload</a></td>
<td>

Renders the given manifest source file and returns the result, with the inputs injected into the template file. Primarily used for testing non-persisted manifests before their creation.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#renderconfigurationmanifestinput">RenderConfigurationManifestInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>instantiateWorkflow</strong></td>
<td valign="top"><a href="#instantiateworkflowpayload">InstantiateWorkflowPayload</a></td>
<td>

Instantiates a workflow with an optional entity (e.g., record or asset reference) and additional data which is passed through the workflow.

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#instantiateworkflowinput">InstantiateWorkflowInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteAccountSandboxOrganization</strong></td>
<td valign="top"><a href="#deleteaccountsandboxorganizationpayload">DeleteAccountSandboxOrganizationPayload</a></td>
<td>

Deletes the given organizations within the specified account. `CUSTOMER` accounts are not supported at this time

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#deleteaccountsandboxorganizationinput">DeleteAccountSandboxOrganizationInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>provisionOrganization</strong></td>
<td valign="top"><a href="#provisionorganizationpayload">ProvisionOrganizationPayload</a></td>
<td>

Creates an organization within the specified account. `CUSTOMER` accounts are not supported at this time

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#provisionorganizationinput">ProvisionOrganizationInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### Account

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestByName</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">name</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestInstallation</strong></td>
<td valign="top"><a href="#configurationmanifestinstallation">ConfigurationManifestInstallation</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestInstallations</strong></td>
<td valign="top"><a href="#configurationmanifestinstallationpaginatedlist">ConfigurationManifestInstallationPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#configurationmanifestinstallationfilterinput">ConfigurationManifestInstallationFilterInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifests</strong></td>
<td valign="top"><a href="#configurationmanifestpaginatedlist">ConfigurationManifestPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>accountType</strong></td>
<td valign="top"><a href="#accounttype">AccountType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#accountorganization">AccountOrganization</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizations</strong></td>
<td valign="top"><a href="#accountorganizationpaginatedlist">AccountOrganizationPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### AccountOrganization

Represents an organization within an account

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AccountOrganizationPaginatedList

A paginated collection of AccountOrganizations.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#accountorganization">AccountOrganization</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### AccountPaginatedList

A paginated collection of Accounts.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#account">Account</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CanceledProvisionOrganizationRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CompletedConfigurationManifestEntityTypeInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logFileDownloadUrl</strong></td>
<td valign="top"><a href="#url">Url</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CompletedConfigurationManifestEntityTypeVersionRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logFileDownloadUrl</strong></td>
<td valign="top"><a href="#url">Url</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>version</strong></td>
<td valign="top"><a href="#configurationmanifestentitytypeversion">ConfigurationManifestEntityTypeVersion</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CompletedConfigurationManifestInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersion</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeInstallations</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeinstallation">ConfigurationManifestEntityTypeInstallation</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>initiatingUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetOrganization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
</tbody>
</table>

### CompletedConfigurationManifestVersionRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityTypeVersionRequests</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeversionrequest">ConfigurationManifestEntityTypeVersionRequest</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>version</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CompletedProvisionOrganizationRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifest

Stores the package of organization configuration, versions, and installations onto organizations

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>creatorUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>latestVersion</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceOrganization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionRequests</strong></td>
<td valign="top"><a href="#configurationmanifestversionrequestpaginatedlist">ConfigurationManifestVersionRequestPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versions</strong></td>
<td valign="top"><a href="#configurationmanifestversionpaginatedlist">ConfigurationManifestVersionPaginatedList</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">pagination</td>
<td valign="top"><a href="#paginationinput">PaginationInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestEntityType

An entity type that can be exported/imported via manifests

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>systemName</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#configurationmanifestentitytypevalue">ConfigurationManifestEntityTypeValue</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestEntityTypeVersion

Represents a snapshot of the source organization's configuration, or the entities in a file-based manifest, limited to a single entity type

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logFileDownloadUrl</strong></td>
<td valign="top"><a href="#url">Url</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationPaginatedList

A paginated collection of ConfigurationManifestInstallations.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#configurationmanifestinstallation">ConfigurationManifestInstallation</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestPaginatedList

A paginated collection of ConfigurationManifests.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#configurationmanifest">ConfigurationManifest</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestVersion

A snapshot of the source organization's configuration, or the entities in a file-based manifest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeVersions</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeversion">ConfigurationManifestEntityTypeVersion</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>manifestFileDownloadUrl</strong></td>
<td valign="top"><a href="#url">Url</a>!</td>
<td>

URL to the rendered configuration manifest YAML

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestVersionPaginatedList

A paginated collection of ConfigurationManifestVersions.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#configurationmanifestversion">ConfigurationManifestVersion</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestVersionRequestPaginatedList

A paginated collection of ConfigurationManifestVersionRequests.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#configurationmanifestversionrequest">ConfigurationManifestVersionRequest</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestFromFilePayload

Autogenerated return type for the createConfigurationManifestFromFile mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersionRequest</strong></td>
<td valign="top"><a href="#configurationmanifestversionrequest">ConfigurationManifestVersionRequest</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestFromOrganizationPayload

Autogenerated return type for the createConfigurationManifestFromOrganization mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersionRequest</strong></td>
<td valign="top"><a href="#configurationmanifestversionrequest">ConfigurationManifestVersionRequest</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestVersionFromFilePayload

Autogenerated return type for the createConfigurationManifestVersionFromFile mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersionRequest</strong></td>
<td valign="top"><a href="#configurationmanifestversionrequest">ConfigurationManifestVersionRequest</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestVersionFromOrganizationPayload

Autogenerated return type for the createConfigurationManifestVersionFromOrganization mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersionRequest</strong></td>
<td valign="top"><a href="#configurationmanifestversionrequest">ConfigurationManifestVersionRequest</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteAccountSandboxOrganizationPayload

Autogenerated return type for the deleteAccountSandboxOrganization mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>deletedOrganizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteConfigurationManifestPayload

Autogenerated return type for the deleteConfigurationManifest mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>deletedConfigurationManifestId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### FailedConfigurationManifestEntityTypeInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>failureReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logFileDownloadUrl</strong></td>
<td valign="top"><a href="#url">Url</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FailedConfigurationManifestEntityTypeVersionRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>failureReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>logFileDownloadUrl</strong></td>
<td valign="top"><a href="#url">Url</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FailedConfigurationManifestInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersion</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeInstallations</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeinstallation">ConfigurationManifestEntityTypeInstallation</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>initiatingUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetOrganization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
</tbody>
</table>

### FailedConfigurationManifestVersionRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityTypeVersionRequests</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeversionrequest">ConfigurationManifestEntityTypeVersionRequest</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>failureReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FailedProvisionOrganizationRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### InstallConfigurationManifestPayload

Autogenerated return type for the installConfigurationManifest mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestInstallation</strong></td>
<td valign="top"><a href="#configurationmanifestinstallation">ConfigurationManifestInstallation</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### InstantiateWorkflowPayload

Autogenerated return type for the instantiateWorkflow mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>workflowInstance</strong></td>
<td valign="top"><a href="#workflowinstance">WorkflowInstance</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Organization

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### OrganizationPaginatedList

A paginated collection of Organizations.

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entries</strong></td>
<td valign="top">[<a href="#organization">Organization</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>pageMetadata</strong></td>
<td valign="top"><a href="#pagemetadata">PageMetadata</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### PageMetadata

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasNext</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>hasPrevious</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>totalEntries</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### PreviewConfigurationManifestPayload

Autogenerated return type for the previewConfigurationManifest mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contents</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ProvisionOrganizationPayload

Autogenerated return type for the provisionOrganization mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>provisionOrganizationRequest</strong></td>
<td valign="top"><a href="#provisionorganizationrequest">ProvisionOrganizationRequest</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RenderConfigurationManifestPayload

Autogenerated return type for the renderConfigurationManifest mutation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contents</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RunningConfigurationManifestEntityTypeInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RunningConfigurationManifestEntityTypeVersionRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RunningConfigurationManifestInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersion</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeInstallations</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeinstallation">ConfigurationManifestEntityTypeInstallation</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>initiatingUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetOrganization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
</tbody>
</table>

### RunningConfigurationManifestVersionRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityTypeVersionRequests</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeversionrequest">ConfigurationManifestEntityTypeVersionRequest</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RunningProvisionOrganizationRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### StoppedConfigurationManifestEntityTypeInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>cancelReason</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### StoppedConfigurationManifestInstallation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersion</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeInstallations</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeinstallation">ConfigurationManifestEntityTypeInstallation</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>finishedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>initiatingUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetOrganization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
</tbody>
</table>

### User

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowInstance

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Inputs

### ConfigurationManifestFileSourceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contents</strong></td>
<td valign="top"><a href="#configurationmanifestyaml">ConfigurationManifestYaml</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#url">Url</a></td>
<td>

Public URL for a configuration manifest YAML file

</td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationEntityTypeSelectionInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>selectedEntityTypes</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypevalue">ConfigurationManifestEntityTypeValue</a>!]</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationFilterFieldReferenceInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>field</strong></td>
<td valign="top"><a href="#configurationmanifestinstallationfilterfield">ConfigurationManifestInstallationFilterField</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationFilterInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>equals</strong></td>
<td valign="top"><a href="#configurationmanifestinstallationfiltermultivaluedcomparisoninput">ConfigurationManifestInstallationFilterMultivaluedComparisonInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>search</strong></td>
<td valign="top"><a href="#filtersearchinput">FilterSearchInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationFilterMultivaluedComparisonInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>left</strong></td>
<td valign="top"><a href="#configurationmanifestinstallationfilterfieldreferenceinput">ConfigurationManifestInstallationFilterFieldReferenceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>right</strong></td>
<td valign="top">[<a href="#configurationmanifestinstallationfiltervalueinput">ConfigurationManifestInstallationFilterValueInput</a>!]!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationFilterValueInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>dateTime</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>now</strong></td>
<td valign="top"><a href="#filternowinput">FilterNowInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>relativeTime</strong></td>
<td valign="top"><a href="#filterrelativetimeinput">FilterRelativeTimeInput</a></td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestFromFileInput

Autogenerated input type for the createConfigurationManifestFromFile mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account the manifest will be created in

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileSource</strong></td>
<td valign="top"><a href="#configurationmanifestfilesourceinput">ConfigurationManifestFileSourceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestFromOrganizationInput

Autogenerated input type for the createConfigurationManifestFromOrganization mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account the manifest will be created in

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceOrganizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Organization to create manifest from. Must be a part of account specified by `account_id`

</td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestVersionFromFileInput

Autogenerated input type for the createConfigurationManifestVersionFromFile mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account of the configuration manifest

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>fileSource</strong></td>
<td valign="top"><a href="#configurationmanifestfilesourceinput">ConfigurationManifestFileSourceInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### CreateConfigurationManifestVersionFromOrganizationInput

Autogenerated input type for the createConfigurationManifestVersionFromOrganization mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account of the configuration manifest

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteAccountSandboxOrganizationInput

Autogenerated input type for the deleteAccountSandboxOrganization mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### DeleteConfigurationManifestInput

Autogenerated input type for the deleteConfigurationManifest mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account of the manifest being deleted

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FilterNowInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>_ignored</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
</tbody>
</table>

### FilterRelativeTimeInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>offset</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### FilterSearchInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>searchString</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### InstallConfigurationManifestInput

Autogenerated input type for the installConfigurationManifest mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account of the manifest being installed

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersionNumber</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Version of manifest to install. Defaults to latest version

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeSelection</strong></td>
<td valign="top"><a href="#configurationmanifestinstallationentitytypeselectioninput">ConfigurationManifestInstallationEntityTypeSelectionInput</a></td>
<td>

Entity types to install. Defaults to all entity types

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parameterInputs</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetAccountId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td>

Account of the organization referenced by `organizationId`. Defaults to the value of `accountId`. Required for cross-account operations

</td>
</tr>
</tbody>
</table>

### InstantiateWorkflowInput

Autogenerated input type for the instantiateWorkflow mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entity</strong></td>
<td valign="top"><a href="#workflowentityinput">WorkflowEntityInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workflowId</strong></td>
<td valign="top"><a href="#identifier">Identifier</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>workflowInstanceData</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
</tbody>
</table>

### PaginationInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>cursor</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>page</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>size</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#paginationinputtype">PaginationInputType</a></td>
<td></td>
</tr>
</tbody>
</table>

### PreviewConfigurationManifestInput

Autogenerated input type for the previewConfigurationManifest mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td>

Account of the manifest being previewed

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersionNumber</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Version of manifest to preview. Defaults to latest version

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organizationId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parameterInputs</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetAccountId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td>

Account of the organization referenced by `organizationId`. Defaults to the value of `accountId`. Required for cross-account operations

</td>
</tr>
</tbody>
</table>

### ProvisionOrganizationInput

Autogenerated input type for the provisionOrganization mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>accountId</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### RenderConfigurationManifestInput

Autogenerated input type for the renderConfigurationManifest mutation

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>fileSource</strong></td>
<td valign="top"><a href="#configurationmanifestfilesourceinput">ConfigurationManifestFileSourceInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>input</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowEntityInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#identifier">Identifier</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#workflowentitytype">WorkflowEntityType</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### AccountType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CUSTOMER</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INTERNAL</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PARTNER</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestEntityTypeValue

The supported entity types that can be exported/imported via manifests

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CATALOG_SITE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHANNELS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHANNEL_MAPPING_ENTRIES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CHANNEL_REFERENCES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONTENT_LOCALES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONTENT_LOCALE_SECURITY_POLICIES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DATA_INHERITANCE_HIERARCHIES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DATA_INHERITANCE_HIERARCHY_LEVEL_TAGS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DEFAULT_LOCALE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DIGITAL_ASSET_SECURITY_POLICIES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ENUMERATED_VALUES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LISTS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LIST_REFERENCES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROPERTIES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROPERTY_GROUPS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RECORD_SECURITY_POLICIES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SCHEMA_RULES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SECURITY_ROLES</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TARGET_SCHEMA_FLAGS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>USERS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>USER_GROUPS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>WORKFLOW</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>WORKFLOW_ORGANIZATION_SETTINGS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>WORKFLOW_STEP_TYPE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>WORKFLOW_TASK_RULE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallationFilterField

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CONFIGURATION_MANIFEST_ID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CREATED_AT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>STATUS</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TARGET_ORGANIZATION_ID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>UPDATED_AT</strong></td>
<td></td>
</tr>
</tbody>
</table>

### PaginationInputType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>CURSOR_NEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PER_PAGE</strong></td>
<td></td>
</tr>
</tbody>
</table>

### WorkflowEntityType

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DIGITAL_ASSET</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RECORD</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### ConfigurationManifestYaml

YAML representation of a configuration manifest in string format

### ID

The `ID` scalar type represents a unique identifier, often used to refetch an object or as key for a cache. The ID type appears in a JSON response as a String; however, it is not intended to be human-readable. When expected as an input type, any string (such as `"4"`) or integer (such as `4`) input value will be accepted as an ID.

### Identifier

ID or External ID

### Int

The `Int` scalar type represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1.

### Iso8601DateTime

An ISO 8601-encoded datetime

### Json

An untyped JSON value

### String

The `String` scalar type represents textual data, represented as UTF-8 character sequences. The String type is most often used by GraphQL to represent free-form human-readable text.

### Url

## Interfaces

### ConfigurationManifestEntityTypeInstallation

Represents an application of manifest into a target organization, limited to a single entity type. Can be used to track the process of installing the manifest into the organization

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestEntityTypeVersionRequest

Represents a request to create a snapshot of the source organization's configuration, or the entities in a file-based manifest, limited to a single entity type

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityType</strong></td>
<td valign="top"><a href="#configurationmanifestentitytype">ConfigurationManifestEntityType</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestInstallation

Represents an application of manifest into a target organization. Can be used to track the process of installing the manifest into the organization

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>configurationManifest</strong></td>
<td valign="top"><a href="#configurationmanifest">ConfigurationManifest</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>configurationManifestVersion</strong></td>
<td valign="top"><a href="#configurationmanifestversion">ConfigurationManifestVersion</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>entityTypeInstallations</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeinstallation">ConfigurationManifestEntityTypeInstallation</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>initiatingUser</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>targetOrganization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConfigurationManifestVersionRequest

Represents a request to create a snapshot of the source organization's configuration, or the entities in a file-based manifest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>entityTypeVersionRequests</strong></td>
<td valign="top">[<a href="#configurationmanifestentitytypeversionrequest">ConfigurationManifestEntityTypeVersionRequest</a>!]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>versionNumber</strong></td>
<td valign="top"><a href="#int">Int</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### ProvisionOrganizationRequest

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isPending</strong></td>
<td valign="top"><a href="#boolean">Boolean</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>startedAt</strong></td>
<td valign="top"><a href="#iso8601datetime">Iso8601DateTime</a>!</td>
<td></td>
</tr>
</tbody>
</table>