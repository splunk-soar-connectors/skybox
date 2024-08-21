[comment]: # "Auto-generated SOAR connector documentation"
# Skybox

Publisher: Splunk  
Connector Version: 1.0.6  
Product Vendor: Skybox Security  
Product Name: Skybox  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 4.6.19142  

This app integrates with Skybox to provide an investigative action

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Skybox asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base_url** |  required  | string | Server URL (e.g. https://myskybox.com)
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

If a CIDR block is specified, the action will return all assets in that range.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**ip** |  required  | IP (or CIDR) to lookup | string | 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.parameter.ip | string |  |   10.41.1.0/24 
action_result.status | string |  |   success  failed 
action_result.message | string |  |  
summary.total_objects | numeric |  |   1 
summary.total_objects_successful | numeric |  |   1 
action_result.data.\*.status | string |  |   Up 
action_result.data.\*.netInterface.\*.type | string |  |   Tunnel 
action_result.data.\*.netInterface.\*.ipAddress | string |  `ip`  |   10.40.0.2 
action_result.data.\*.netInterface.\*.id | numeric |  |   10568 
action_result.data.\*.netInterface.\*.name | string |  |   Tunnel222 
action_result.data.\*.type | string |  |   Router 
action_result.data.\*.name | string |  |   Skytest_Router 
action_result.data.\*.osVendor | string |  |   Cisco 
action_result.data.\*.primaryIp | string |  `ip`  |   10.40.0.2 
action_result.data.\*.interfaces | numeric |  |   4 
action_result.data.\*.routingRules | numeric |  |   6 
action_result.data.\*.accessRules | numeric |  |   3 
action_result.data.\*.vulnerabilities.\*.comment | string |  |  
action_result.data.\*.vulnerabilities.\*.createdBy | string |  |   skyboxview 
action_result.data.\*.vulnerabilities.\*.lastScanTime | numeric |  |   1449763906560 
action_result.data.\*.vulnerabilities.\*.hostName | string |  `host name`  |   Skytest_Router 
action_result.data.\*.vulnerabilities.\*.serviceName | string |  |   IOS 
action_result.data.\*.vulnerabilities.\*.id | numeric |  |   25941 
action_result.data.\*.vulnerabilities.\*.risk | string |  |   NO_RISK 
action_result.data.\*.vulnerabilities.\*.severity | string |  |   High 
action_result.data.\*.vulnerabilities.\*.title | string |  |   [cisco-sa-20120926-nat] Cisco IOS NAT Implementation Allows Remote DoS 
action_result.data.\*.vulnerabilities.\*.lastModifiedBy | string |  |   skyboxview 
action_result.data.\*.vulnerabilities.\*.servicePorts | string |  |  
action_result.data.\*.vulnerabilities.\*.networkNames | string |  |   10.11.0.2_10.40.0.2,,0.0.0.0_0.0.0.0 
action_result.data.\*.vulnerabilities.\*.status | string |  |   Found 
action_result.data.\*.vulnerabilities.\*.hostId | numeric |  |   10376 
action_result.data.\*.vulnerabilities.\*.description | string |  |   The NAT implementation in Cisco IOS 12.2, 12.4, and 15.0 through 15.2 allows remote attackers to cause a denial of service (device reload) via transit IP packets, aka Bug ID CSCtr46123. 
action_result.data.\*.vulnerabilities.\*.discoveryMethod | string |  |   VULNERABILITY_DETECTOR 
action_result.data.\*.vulnerabilities.\*.lastModificationTime | numeric |  |   1427987506176 
action_result.data.\*.vulnerabilities.\*.vulnerabilityTypeId.id | numeric |  |   36257 
action_result.data.\*.vulnerabilities.\*.vulnerabilityTypeId.dictionary | string |  |   SBV 
action_result.data.\*.vulnerabilities.\*.hostIp | string |  `ip`  |   10.40.0.2 
action_result.data.\*.vulnerabilities.\*.exposure | string |  |   Mitigated 
action_result.data.\*.vulnerabilities.\*.creationTime | numeric |  |   1428837875712 
action_result.data.\*.vulnerabilities.\*.networkGroupNames | string |  |  
action_result.data.\*.vulnerabilities.\*.cve | string |  |   CVE-2012-4619 
action_result.data.\*.services | numeric |  |   4 
action_result.data.\*.osVersion | string |  |   12.4 
action_result.data.\*.os | string |  |   IOS 
action_result.data.\*.id | numeric |  |   10376 
action_result.data.\*.vulnerabilities.\*.scannerId | string |  |   SBV/54866 