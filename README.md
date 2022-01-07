[comment]: # "Auto-generated SOAR connector documentation"
# Skybox

Publisher: Splunk  
Connector Version: 1\.0\.4  
Product Vendor: Skybox Security  
Product Name: Skybox  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.6\.19142  

This app integrates with Skybox to provide an investigative action

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Skybox asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base\_url** |  required  | string | Server URL \(e\.g\. https\://myskybox\.com\)
**username** |  required  | string | Username
**password** |  required  | password | Password

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[lookup ip](#action-lookup-ip) - Checks Skybox for the existence of the IP among the model's assets  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'lookup ip'
Checks Skybox for the existence of the IP among the model's assets

Type: **investigate**  
Read only: **True**

If a CIDR block is specified, the action will return all assets in that range\.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP \(or CIDR\) to lookup | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.parameter\.ip | string | 
action\_result\.status | string | 
action\_result\.message | string | 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 
action\_result\.data\.\*\.status | string | 
action\_result\.data\.\*\.netInterface\.\*\.type | string | 
action\_result\.data\.\*\.netInterface\.\*\.ipAddress | string |  `ip` 
action\_result\.data\.\*\.netInterface\.\*\.id | numeric | 
action\_result\.data\.\*\.netInterface\.\*\.name | string | 
action\_result\.data\.\*\.type | string | 
action\_result\.data\.\*\.name | string | 
action\_result\.data\.\*\.osVendor | string | 
action\_result\.data\.\*\.primaryIp | string |  `ip` 
action\_result\.data\.\*\.interfaces | numeric | 
action\_result\.data\.\*\.routingRules | numeric | 
action\_result\.data\.\*\.accessRules | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.comment | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.createdBy | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.lastScanTime | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.hostName | string |  `host name` 
action\_result\.data\.\*\.vulnerabilities\.\*\.serviceName | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.id | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.risk | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.severity | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.title | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.lastModifiedBy | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.servicePorts | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.networkNames | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.status | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.hostId | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.description | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.discoveryMethod | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.lastModificationTime | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.vulnerabilityTypeId\.id | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.vulnerabilityTypeId\.dictionary | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.hostIp | string |  `ip` 
action\_result\.data\.\*\.vulnerabilities\.\*\.exposure | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.creationTime | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.networkGroupNames | string | 
action\_result\.data\.\*\.vulnerabilities\.\*\.cve | string | 
action\_result\.data\.\*\.services | numeric | 
action\_result\.data\.\*\.osVersion | string | 
action\_result\.data\.\*\.os | string | 
action\_result\.data\.\*\.id | numeric | 
action\_result\.data\.\*\.vulnerabilities\.\*\.scannerId | string | 