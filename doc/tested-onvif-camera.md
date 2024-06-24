# Tested Onvif Camera
The following table shows the tested Onvif cameras with Onvif functions:

* 'O' means the function works for the camera.
* 'X' means the function not work for the camera. The camera might not perform the request or return empty response.

| Feature                            | Onvif Web Service | Onvif Function                      | Hikvision DFI6256TE | Tapo C200 | BOSCH DINION IP starlight 6000 HD | GeoVision GV-BX8700 | Honeywell HC30WB5R1 |
|------------------------------------|-------------------|-------------------------------------|---------------------|-----------|-----------------------------------|---------------------|--------------|
| User Authentication                | Core              | **WS-Usernametoken Authentication** | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | **HTTP Digest**                     | O                   | X         | O                                 | X                   |   X          |
| Auto Discovery                     | Core              | **WS-Discovery**                    | O                   | O         | O                                 | O                   |   O          |
|                                    | Device            | GetDiscoveryMode                    | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | SetDiscoveryMode                    | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | GetScopes                           | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | SetScopes                           | O                   | O         | O                                 | O                   |   X          |
|                                    |                   | AddScopes                           | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | RemoveScopes                        | O                   | X         | O                                 | O                   |   O          |
| Network Configuration              | Device            | GetHostname                         | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | SetHostname                         | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | GetDNS                              | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | SetDNS                              | O                   | X         | O                                 | O                   |   X          |
|                                    |                   | **GetNetworkInterfaces**            | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | **SetNetworkInterfaces**            | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | GetNetworkProtocols                 | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | SetNetworkProtocols                 | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | **GetNetworkDefaultGateway**        | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | **SetNetworkDefaultGateway**        | O                   | X         | O                                 | O                   |   X          |
| System Function                    | Device            | **GetDeviceInformation**            | O                   | O         | O                                 | O                   |   O
|                                    |                   | GetSystemDateAndTime                | O                   | O         | O                                 | O                   |   O
|                                    |                   | SetSystemDateAndTime                | O                   | X         | O                                 | O                   |   X
|                                    |                   | SetSystemFactoryDefault             | O                   | O         | O                                 | O                   |
|                                    |                   | Reboot                              | O                   | O         | O                                 | O                   |   O
| User Handling                      | Device            | **GetUsers**                        | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | **CreateUsers**                     | O                   | X         | O                                 | O                   |   O          |
|                                    |                   | **DeleteUsers**                     | O                   | X         | O                                 | O                   |   X          |
|                                    |                   | **SetUser**                         | O                   | X         | O                                 | O                   |   O          |
| Metadata Configuration             | Media             | GetMetadataConfigurations           | O                   | X         | O                                 | O                   |   X          |
|                                    |                   | GetMetadataConfiguration            | O                   | X         | O                                 | O                   |   X         |
|                                    |                   | GetCompatibleMetadataConfigurations | O                   | X         | O                                 | O                   |   X          |
|                                    |                   | **GetMetadataConfigurationOptions** | O                   | X         | O                                 | O                   |   X          |
|                                    |                   | AddMetadataConfiguration            | O                   | X         | O                                 | O                   |   X         |
|                                    |                   | RemoveMetadataConfiguration         | O                   | X         | O                                 | O                   |   X         |
|                                    |                   | **SetMetadataConfiguration**        | O                   | X         | O                                 | O                   |   X          |
| Video Streaming                    | Media             | **GetProfiles**                     | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | **GetStreamUri**                    | O                   | O         | O                                 | O                   |   O          |
| VideoEncoder  Config               | Media             | GetVideoEncoderConfiguration        | O                   | O         | O                                 | O                   |   O          |
|                                    |                   | **SetVideoEncoderConfiguration**    | O                   | X         | O                                 | O                   |   X          |
|                                    |                   | GetVideoEncoderConfigurationOptions | O                   | O         | O                                 | O                   |   O          |
| PTZ Node                           | PTZ               | GetNodes                            | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | GetNode                             | X                   | O         | X                                 | X                   |   X          |
| PTZ Configuration                  | PTZ               | GetConfigurations                   | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | GetConfiguration                    | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | GetConfigurationOptions             | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | SetConfiguration                    | X                   | X         | X                                 | X                   |   X          |
|                                    | Media             | AddPTZConfiguration                 | X                   | X         | X                                 | X                   |   X          |
|                                    | Media             | RemovePTZConfiguration              | X                   | X         | X                                 | X                   |   X          |
| PTZ Actuation                      | PTZ               | AbsoluteMove                        | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | RelativeMove                        | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | ContinuousMove                      | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | Stop                                | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | GetStatus                           | X                   | O         | X                                 | X                   |   X          |
| PTZ Preset                         | PTZ               | SetPreset                           | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | GetPresets                          | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | GotoPreset                          | X                   | O         | X                                 | X                   |   X          |
|                                    |                   | RemovePreset                        | X                   | O         | X                                 | X                   |   X          |
| PTZ Home Position                  | PTZ               | GotoHomePosition                    | X                   | X         | X                                 | X                   |   X          |
|                                    |                   | SetHomePosition                     | X                   | X         | X                                 | X                   |   X          |
| PTZ AuxiliaryOperations            | PTZ               | SendAuxiliaryCommand                | X                   | X         | X                                 | X                   |   X          |
| Event Handling                     | Event             | Notify                              | O                   | X         | O                                 | X                   |   X          |
|                                    |                   | Subscribe                           | O                   | X         | O                                 | X                   |   X          |
|                                    |                   | Renew                               | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | Unsubscribe                         | O                   | X         | O                                 | X                   |   X          |
|                                    |                   | CreatePullPointSubscription         | O                   | X         | O                                 | X                   |   X          |
|                                    |                   | PullMessages                        | O                   | X         | O                                 | X                   |   X          |
|                                    |                   | TopicFilter                         | O                   | X         | O                                 | X                   |   X          |
|                                    |                   | MessageContentFilter                | X                   | X         | X                                 | X                   |   X          |
| Configuration of Analytics profile | Media2            | GetProfiles                         | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | GetAnalyticsConfigurations          | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | AddConfiguration                    | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | RemoveConfiguration                 | X                   | X         | O                                 | X                   |   X          |
| Analytics Module configuration     | Analytics         | GetSupportedAnalyticsModules        | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | GetAnalyticsModules                 | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | CreateAnalyticsModules              | X                   | X         | X                                 | X                   |   X          |
|                                    |                   | DeleteAnalyticsModules              | X                   | X         | X                                 | X                   |   X          |
|                                    |                   | GetAnalyticsModuleOptions           | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | ModifyAnalyticsModules              | X                   | X         | O                                 | X                   |   X          |
| Rule configuration                 | Analytics         | GetSupportedRules                   | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | GetRules                            | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | CreateRules                         | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | DeleteRules                         | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | GetRuleOptions                      | X                   | X         | O                                 | X                   |   X          |
|                                    |                   | ModifyRules                         | X                   | X         | O                                 | X                   |   X          |
