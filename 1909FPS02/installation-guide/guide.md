# Main part

## Step 1 - Import the transports

Please import the transport requests that Fiori Tracker team provides.

## Step 2 - Activate services

**2.1** Run **SICF** transaction and activate those ICF nodes:<br/>
Path: **/default_host/sap/bc/ui5_ui5/sap/**
- zfioritracker
- zfioristatslog
- zfiorimfuastart
- zfioriappstart
- zfioriappexplorer
- zfioriissuelog
- zfioriodatamng<br/>

Path: **/default_host/sap/opu/odata/sap/**
- ZFIORITRACKER_SRV

## Step 3 - Assign the roles

In **PFCG** transaction assign the authorization roles to the users that you want to use for starting Fiori Tracker apps:
- ZFT_ADMIN
- ZFT_USER

## Step 4 - Add intervals for number ranges

**4.1** Run **ZFTSETUP** transaction.<br />
**4.2** Choose **"Create number range intervals"**.<br />
**4.3** If every objects' intervals have been changed successfully - you should see below screen.<br />

!> **Current index** for each object should be set to 1.

![](../res/guide_intervals.png)

## Step 5 - Create initial area codes

In this step, you can create initial codes for your business areas. All applications, business catalogs, and roles could be assigned to a specific area (please find example area codes below).

![](../res/guide_area_codes.jpg)

## Step 6 - Create default initial data

In this step, you create default initial data for Fiori Tracker based on the information you have provided in the previous steps.

## Step 7 - Modify configuration

In this step you are able to modify Fiori Tracker configuration:
- CatalogNamingRule - you can specify your rules for catalog naming
- CatalogsImportIsTechnicalCatalogCheckZC
Sets on and off the naming convention check with rules set in parameter "CatalogNamingRule." The system verifies the entry in the catalog header edit mode and import from file function.
- IsProductive - on productive system should be set to **true**, on test and development to **false**. 
Once set to false Fiori Tracker apps will display a warning that is meant to help users to realize that they are not looking at productive data and avoid mistakes
- ProductiveSystemAddress - **yourhost:port**
- ProductiveSystemId - system ID
- SapVersion - your S/4 HANA version

![](../res/config.png)

## Step 8 - Modify application types

In this step, you can change application types. We recommend using our proposition of them based on the SAP Fiori apps reference library (please find them below).

![](../res/app_types.png)

## Step 9 - Modify sign off types

In this step, you can change sign off types. They should be relevant to the steps of your development process (please find the example below).

![](../res/sign_off_types.png)

## Step 10 - Modify provisioning types

In this step, you can change provisioning types. They should be relevant to your system landscape (please find the example below).

![](../res/provisioning_types.png)

## Step 11 - Modify user responsible for an area

In this step, you can change users responsible for specific business areas f.e. stream leads.

![](../res/user_to_area.png)

## Step 12 - Modify user responsible for the provisioning of a specific set

In this step, you can change users responsible for the provisioning of a specific set f.e. applications.

![](../res/user_to_type.png)

## Step 13 - Check if the Fiori Tracker applications run correctly

There are two ways to start Fiori Tracker applications:

From your SAP Fiori Launchpad:
- Login and start the SAP Fiori Launchpad with the user that you have configured in Step 3 of the installation guide.

![](../res/ft_flp.png)

You can also start the Fiori Tracker as an standalone application:
- **yourhost:port**/sap/bc/ui5_ui5/sap/zfioritracker/</br>
f.e. https://demo.fioritracker.org/sap/bc/ui5_ui5/sap/zfioritracker/

![](../res/ft_standalone.png)
