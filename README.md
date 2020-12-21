# Tealium Data Enrichment template for Google Tag Manager

## Overview

This is the Google Tag Manager template for the Tealium Data Enrichment tag.

The Tealium Data Enrichment tag allows you to enable and configure client-side data enrichment for Tealium's Customer Data Hub (CDH) on your website using Google Tag Manager.  This tag reads server-side attributes for a Visitor and then brings these into Local Storage for use client-side in the web browser.

For more information on Tealium's CDH, please visit [Tealium's Learning Community](https://community.tealiumiq.com/t5/Customer-Data-Hub/Introduction-to-Customer-Data-Hub/ta-p/17571)

For more information on Tealium's Data Layer Enrichment API, please visit [Tealium's Learning Community](https://community.tealiumiq.com/t5/Customer-Data-Hub/Data-Layer-Enrichment-Public-API/ta-p/155)

## Quickstart Configuration

1. Search the Google Tag Manager Community Template Gallery for "Tealium Data Enrichment"
2. Add this template
3. Create a new tag from this template
4. Enter the Tealium Account and Profile obtained from Tealium's CDH
5. Subscribe your tag to the "All Pages (Page View)" event.
6. Create a custom Variable that will return specific values from Local Storage

## Advanced Configuration

Tealium recommends triggering this tag for the built-in All Pages event.  Keep in mind that it may take multiple page views before visitor data enrichment service returns data.  Usually, the first (or second) page writes data to Local Storage and then the third page view will have this information available for client-side use.

Tealium Data Enrichment tag template also allows for advanced configuration settings:

1. First-party endpoint

If your network team has worked with Tealium to configure a first-party data endpoint, then you should enter the endpoint here.  Consult your Account Manager or Implementation Engineer for more information.

**IMPORTANT**

For first-party configurations, you will need to edit the tag Template "Permissions" section before you add the tag itself (Templates -> Template Editor -> Permissions -> Injects Scripts).

2. Add Enrichment Data to dataLayer 

This checkbox is used if you want to have this tag automatically call dataLayer.push when it finds the enrichment data in Local Storage.  More likely you would use a set of "User Defined Variables" to retreive specific items from Local Storage.  For example, you may want to create a specific Variable (Custom JavaScript) that determines if a Badge is true or false.  Then use this Variable as part of another tag's configuration or Trigger.

## Additional Resources

**[Tealium Collect Tag in Google Tag Manager Documentation](https://docs.tealium.com/platforms/google-tag-manager/install/)**

## Copyright and license

Copyright 2020 Tealium Inc. All rights reserved.

Licensed under the **[Apache License, Version 2.0][license]** (the "License");
you may not use this software except in compliance with the License.

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

