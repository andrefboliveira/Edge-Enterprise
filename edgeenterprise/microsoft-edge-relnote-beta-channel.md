---
title: "Microsoft Edge release notes for Beta Channel"
ms.author: aguta
author: dan-wesley
manager: srugh
ms.date: 01/29/2021
audience: ITPro
ms.topic: conceptual
ms.prod: microsoft-edge
ms.localizationpriority: high
ms.collection: M365-modern-desktop
description: "Microsoft Edge release notes for Beta Channel"
---

# Release notes for Microsoft Edge Beta Channel

These release notes provide information about new features and non-security updates that are included in the Microsoft Edge Beta Channel. Archived versions of these release notes are available [here](microsoft-edge-relnote-archive-beta-channel.md).

## Version 88.0.705.56: January 29

Fixed various bugs and performance issues.

## Version 88.0.705.49: January 20

Fixed various bugs and performance issues.

## Version 88.0.705.45: January 15

Fixed various bugs and performance issues.

## Version 88.0.705.41: January 11

Fixed various bugs and performance issues.

## Version 88.0.705.29: December 21

Fixed various bugs and performance issues.

<!-- begin major 88 -->
## Version 88.0.705.18: December 9

### Feature updates

- **Deprecations:**

  - Deprecate support for FTP protocol. Support for the legacy FTP protocol has been removed from Microsoft Edge. Attempting to navigate to an FTP link will result in the browser directing the Operating System to open an external application to handle the FTP link. Alternatively, IT administrators can configure Microsoft Edge to use IE Mode for sites that rely on the FTP protocol.
  - Adobe Flash support will be removed. Starting with Microsoft Edge Beta version 88, Adobe Flash capability and support will be removed. Learn more: [Update on Adobe Flash Player End of Support - Microsoft Edge Blog (windows.com)](https://blogs.windows.com/msedgedev/2020/09/04/update-adobe-flash-end-support/)

- **Authentication:**

  - Single Sign On (SSO) now available for Azure Active Directory (Azure AD) accounts and Microsoft Account (MSA) on macOS and down-level Windows. A user signed in on Microsoft Edge on either macOS or down-level Microsoft Windows (7, 8.1) will now get automatically signed into websites that are configured to allow single sign on with Work and Microsoft accounts (e.g., bing.com, office.com, msn.com, outlook.com).<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.
  - Automatically switch users on macOS to their work profile for sites that authenticate with their work account. Starting with Microsoft Edge version 88, we provide the ability to switch sites that authenticate with a user’s work profile on macOS.<br>Note: A user may have to sign out and then sign back in if they'd signed into Microsoft Edge in a version prior to Microsoft Edge 88 to leverage this feature.

- Kiosk mode option to end session. The "End session" button is now available in a kiosk mode public browsing experience. This feature ensures that browser data and settings are deleted when Microsoft Edge is closed. Learn more about kiosk mode features and roadmap, [Configure Microsoft Edge kiosk mode](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode).

- **Security and Privacy:**

  - Alerts are generated if a user's password is found in an online leak. User passwords are checked against a repository of known-breached credentials and sends the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.
  - Automatically upgrade mixed content. Secure pages delivered over HTTPS may contain references images that are served over non-secure HTTP. To improve privacy and security in Microsoft Edge 88, those images will be retrieved over HTTPS instead. If the image is not available over HTTPS, it will not be loaded.
  - View site permissions by site and by recent activity. Starting with Microsoft Edge 88, users will be able to manage site permissions more easily. They will be able to view permissions by web site rather than just permission type. Additionally, we’ve added a recent activity section that will show a user all the recent changes to their site permissions.
  - Increased controls for browser cookies. Starting with Microsoft Edge 88, users can delete third party cookies without affecting first party cookies. Users will also be able to filter their cookies by first or third party and sort by name, number of cookies, and the amount of data stored and last modified.

- **Performance:**

  - Improve browser performance with sleeping tabs. Sleeping tabs improves browser performance by putting inactive tabs to sleep to free up system resources like memory and CPU so active tabs or other applications can use them. Users can prevent sites from going to sleep and configure the length of time before an inactive tab goes to sleep. To keep users in their flow, there are also heuristics to prevent certain sites from going to sleep, such as intranet sites. This feature is limited to a randomly selected group of users who have enabled experimentation. We are planning to have the sleeping tabs feature enabled by default with Microsoft Edge version 89. This feature can be managed with group policies.
  - Improve Microsoft Edge startup speed with startup boost. To improve Microsoft Edge startup speed, we’ve developed a feature named startup boost. Startup boost makes Microsoft Edge launch faster by enabling Microsoft Edge to run in the background. Note: This feature is limited to a randomly selected group of users who have enabled experimentation. These users are giving feedback to the feature team.

- **Productivity:**

  - Improve productivity and multi-tasking with vertical tabs. As the number of horizontal tabs grows, site titles start to get cut off and tab controls are lost as each tab shrinks. This interrupts user workflow as they spend more time finding, switching, and managing their tabs and less time on the task at hand. Vertical tabs let users move their tabs to the side, where vertically aligned icons and longer site titles make it easier to quickly scan, identify and switch to the tab they want to open.
  - Auto filling the date of birth field. Microsoft Edge already helps save time and effort while filling out forms and creating accounts online by auto filling user data such as addresses, names, phone numbers, etc. Microsoft Edge now supports the date of birth field which users can save and auto fill. A user can view, edit and delete this information anytime in their profile settings.
  - Improvements to Recently closed in History. Recently closed now keeps the last 25 tabs and windows from any past browsing session rather than just the previous session. Users can select Recently closed in the new History experience to see all the tabs that were open.
  - “Your day at a glance” feature enabled by default. Starting with Microsoft Edge version 88, information workers can benefit from intelligent productivity features on their New tab page (NTP). We offer users signed in with their work or school account personalized and relevant content powered by their M365 Graph. Users can quickly scan their “Your day at a glance” modules to easily track their meetings and recent work as well as quickly launch the applications they want to use.

- **PDF:**

  - PDF document display in book view (two page). Starting with Microsoft Edge version 88, users can view PDF documents in a single page or in the two page book view. To change the view, click the **Page View** button in the toolbar.
  - Anchored text notes support for PDF files. Starting with Microsoft Edge version 87, users can add typed text notes on any piece of text in PDF files.
  - Smoother text selection experience in PDF documents. Users will get a smoother and consistent text selection experience across PDF documents opened in Microsoft Edge.
  - View webpages saved as PDF files in the Downloads bar. Users can now view the PDF files generated by setting "Save as PDF" as the printer destination for webpages in the Downloads bar.

- **Fonts:**

  - Browser icons are updated to the Fluent design system. As part of our continued work around Fluent Design in the browser, we've made changes to closer align icons to the new Microsoft icon system. These changes will impact many of our high-touch user interfaces, including tabs, address bar, as well as navigational and wayfinding icons found in our various menus.
  - Improved font rendering. Text rendering is improved for better clarity and to reduce blurriness.

### Policy updates

#### New policies

Sixteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [BlockExternalExtensions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#blockexternalextensions) - Blocks external extensions from being installed.
- [InternetExplorerIntegrationLocalFileAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileallowed) - Allow launching of local files in Internet Explorer mode.
- [InternetExplorerIntegrationLocalFileExtensionAllowList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileextensionallowlist) - Open local files in Internet Explorer mode file extension allow list.
- [InternetExplorerIntegrationLocalFileShowContextMenu](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlocalfileshowcontextmenu) - Show context menu to open a link in Internet Explorer mode.
- [IntranetRedirectBehavior](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#intranetredirectbehavior) - Intranet Redirection Behavior.
- [PrinterTypeDenyList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#printertypedenylist) - Disable printer types on the deny list.
- [ShowMicrosoftRewards](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#showmicrosoftrewards) - Show Microsoft Rewards experiences.
- [SleepingTabsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsenabled) - Configure Sleeping Tabs.
- [SleepingTabsTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabstimeout) - Set the background tab inactivity timeout for Sleeping Tabs.
- [SleepingTabsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sleepingtabsblockedforurls) - Block Sleeping Tabs on specific sites.
- [StartupBoostEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#startupboostenabled) - Enable startup boost.
- [UpdatePolicyOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#updatepolicyoverride) - Specifies how Microsoft Edge Update handles available updates from Microsoft Edge.
- [VerticalTabsAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#verticaltabsallowed) - Configures availability of a vertical layout for tabs on the side of the browser.
- [WebRtcAllowLegacyTLSProtocols](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtcallowlegacytlsprotocols) - Allow legacy TLS/DTLS downgrade in WebRTC.

#### Deprecated policies

The following policies are deprecated.

- [ProactiveAuthEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proactiveauthenabled) - Enable Proactive Authentication.
- [ProxyBypassList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxybypasslist) - Configure proxy bypass rules.
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode) - Configure proxy server settings.
- [ProxyPacUrl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxypacurl) - Set the proxy .pac file URL.
- [ProxyServer](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxyserver) - Configure address or URL of proxy server.
- [WebDriverOverridesIncompatiblePolicies](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webdriveroverridesincompatiblepolicies) - Allow WebDriver to Override Incompatible Policies.

#### Obsoleted policies

The following policies are obsoleted.

- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting) - Default Adobe Flash setting.
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls) - Allow the Adobe Flash plug-in on specific sites.
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls) - Block the Adobe Flash plug-in on specific sites.
- [RunAllFlashInAllowMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#runallflashinallowmode) - Extend Adobe Flash content setting to all content.

<!-- end major 88 -->

## Version 87.0.664.55: December 3

Fixed various bugs and performance issues. The following new feature is supported in this release.

- **Alerts are generated if a user's password is found in an online leak**. User passwords are checked against a repository of known-breached credentials and sends the user an alert if a match is found. To ensure security and privacy, user passwords are hashed and encrypted when they're checked against the database of leaked credentials.

## Version 87.0.664.52: November 30

Fixed various bugs and performance issues.

## Version 87.0.664.40: November 18

Fixed various bugs and performance issues.

## Version 87.0.664.36: November 16

Fixed various bugs and performance issues.

## Version 87.0.664.30: November 9

Fixed various bugs and performance issues.

## Version 87.0.664.24: November 2

Fixed various bugs and performance issues.

## Version 87.0.664.18: October 26

Fixed various bugs and performance issues.

<!-- begin major 87 -->
## Version 87.0.664.12: October 20

### Feature updates

- **Kiosk mode privacy features enabled**. Starting with Microsoft Edge version 87 kiosk mode features that will help enterprises around the privacy of user data will be enabled. These features will enable experiences such as clear the user data on exit, delete downloaded files and to reset the configured start experience after a specified amount of idle time. Learn more about how to [Configure Microsoft Edge kiosk mode](https://docs.microsoft.com/deployedge/microsoft-edge-configure-kiosk-mode)
- **ClickOnce deployment enabled by default**. ClickOnce is enabled by default in Microsoft Edge 87, which reduces the barriers for enterprises to deploy software and better align with Microsoft Edge Legacy browser behavior. Starting in Microsoft Edge 87, the ClickOnceEnabled policy's "Not configured" state will reflect the new default ClickOnce state of Enabled (as compared to the previous default state of Disabled).
- **The enterprise new tab page (NTP) integrates productivity with customizable, work-relevant feed content**. The enterprise NTP blends the Office 365 productivity page we offer to users signed in with their work or school account with personalized, work-relevant company and industry feeds that are organized in a single page. Users will be able to recognize the familiar Office 365 content and Microsoft Search for Business powered by Bing. In addition, they can easily flip to a customizable "My Feed" with content and modules that are relevant to the user, their company, or their industry, as well as a selection of other feeds that the organization has made available. [Learn more](https://docs.microsoft.com/microsoft-365/admin/manage/manage-industry-news?view=o365-worldwide&preserve-view=true).

- **Privacy and Security:**

  - Support TLS Token Binding for policy-configured sites. TLS Token binding helps prevent token theft attacks to ensure that cookies can't be reused from a device other than the device upon which they were initially set. The use of TLS token binding requires setting the [AllowTokenBindingForUrls](https://docs.microsoft.com/deployedge/microsoft-edge-policies#allowtokenbindingforurls) policy and requires that the sites listed support this feature.

- **Keyboard support for highlighter on PDF files**. Users can use their keyboard keys to highlight any text on a PDF.

- **Printing:**

  - Choose which side to flip on when printing on both sides. Users can choose to flip on the long side or the short side of a sheet when printing on both sides.
  - Choose print rasterization mode for the enterprise. Control how Microsoft Edge prints to a non-PostScript printer on Windows. Sometimes print jobs on non-PostScript printers need to be rasterized to print correctly. The print options are "Full" and "Fast".

### Policy updates

#### New policies

Ten new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://www.microsoft.com/edge/business/download). The following new policies were added.

- [ConfigureFriendlyURLFormat](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configurefriendlyurlformat) - Configure the default paste format of URLs copied from Microsoft Edge, and determine if additional formats will be available to users.
- [EdgeShoppingAssistantEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#edgeshoppingassistantenabled) - Shopping in Microsoft Edge Enabled.
- [HideInternetExplorerRedirectUXForIncompatibleSitesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#hideinternetexplorerredirectuxforincompatiblesitesenabled) - Hide the one-time redirection dialog and the banner on Microsoft Edge.
- [KioskAddressBarEditingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskaddressbareditingenabled) - Configure address bar editing for kiosk mode public browsing experience.
- [KioskDeleteDownloadsOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#kioskdeletedownloadsonexit) - Delete files downloaded as part of kiosk session when Microsoft Edge closes.
- [PasswordRevealEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordrevealenabled) - Enable the Password reveal button.
- [RedirectSitesFromInternetExplorerPreventBHOInstall](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerpreventbhoinstall) - Prevent install of the BHO to redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [RedirectSitesFromInternetExplorerRedirectMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#redirectsitesfrominternetexplorerredirectmode) - Redirect incompatible sites from Internet Explorer to Microsoft Edge.
- [SpeechRecognitionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#speechrecognitionenabled) - Configure Speech Recognition.
- [WebCaptureEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webcaptureenabled) - Enable the web capture feature in Microsoft Edge.

#### Deprecated Policy

[NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype) - Configure the Microsoft Edge new tab page experience.

#### Obsoleted Policy

[EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures) - Re-enable deprecated web platform features for a limited time.

<!-- end major 87 -->

## Version 86.0.622.43: October 16

Fixed various bugs and performance issues.

## Version 86.0.622.36: October 7

Fixed various bugs and performance issues.

## Version 86.0.622.31: October 1

Fixed various bugs and performance issues.

## Version 86.0.622.28: September 28

Fixed various bugs and performance issues.

## Version 86.0.622.15: September 14

Fixed various bugs and performance issues.

## Version 86.0.622.11: September 9

### Feature updates

* **Internet Explorer mode:**

   * Let users use the Microsoft Edge User Interface (UI) to test sites in Internet Explorer mode. Beginning with Microsoft Edge version 86, administrators can enable a UI option for their users to load a tab in Internet Explorer mode for testing purposes or as a stopgap until sites are added to the site list XML.

* **Delete downloads from disk using download manager.** Users are now able to delete their downloaded files from their disk without leaving the browser. The new Delete downloads functionality exists within the context menu of downloads shelf or the downloads page.

* **Roll back to previous Microsoft Edge version.** The rollback feature lets administrators revert to a known good version of Microsoft Edge if there's an issue in the latest version of Microsoft Edge.
[Learn more](edge-learnmore-rollback.md).

* **Enforce enabling Sync by default across the enterprise.**  Administrators can enable synchronization for Azure Active Directory (Azure AD) accounts by default with the [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) policy.

* **PDF updates:**

  * Table of contents for PDF Documents. Beginning with version 86, Microsoft Edge has added support for table of contents that lets users easily navigate through PDF documents.
  * Access all PDF functionalities on small form factor screens. Access all the capabilities of the Microsoft Edge PDF reader on devices with small screen sizes.
  * Pen support for highlighter on PDF files. With this update, users can use their digital pen to directly highlight text on PDF files, in the same way they would with a physical highlighter and paper.
  * Improved PDF scrolling. You will now be able to experience stutter free scrolling while navigating through long PDF documents.

* **Automatic profile switching on Windows 7, 8, and 8.1.** The automatic profile switching currently available in Microsoft Edge on Windows 10 is extended to downlevel Windows (Windows 7, 8,and  8.1). For more information, see the [automatic profile switching](https://blogs.windows.com/msedgedev/2020/04/30/automatic-profile-switching/) blog post.

* **Users will see auto complete suggestions when they start typing a search query on the Microsoft Edge Add-ons website.** Auto complete will help users quickly complete their search query without having to type the entire string. This will be helpful because users won't have to remember correct spellings and they can choose from the available options that are displayed.

* **Remove the HTML5 Application Cache API.**  Beginning with Microsoft Edge version 86, the legacy Application Cache API that enables offline use of web pages is being removed from Microsoft Edge. Web Developers should review the [WebDev documentation](https://web.dev/appcache-removal/) for information on replacing  the Application Cache API with Service Workers.  Important: You can request an [AppCache OriginTrial Token](https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673) that allows sites to continue to use the deprecated Application Cache API until Microsoft Edge version 90.

* **Security:**

  * Secure DNS (DNS-over-HTTPS) Support.  Beginning with Microsoft Edge version 86, settings to control Secure DNS on un-managed devices is available. These settings aren't accessible to users on managed devices, but IT admins can enable or disable Secure DNS using the [dnsoverhttpsmode](https://docs.microsoft.com/deployedge/microsoft-edge-policies#dnsoverhttpsmode) group policy.


* **Add a custom image to the New Tab Page (NTP) using a group policy.** Beginning with Microsoft Edge version 86 the NTP has an option to replace the default image with a custom user-supplied image. The ability to manage the properties of this image is also supported by the group policy.

* **Match customized keyboard shortcuts to VS Code.** Microsoft Edge DevTools now supports customizing keyboard shortcuts in the DevTools to match with your editor/IDE. (In Microsoft Edge 84, we added the ability to match DevTools keyboard shortcuts to VS Code).

* **Replace [MetricsReportingEnabled]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) and [SendSiteInformationToImproveServices]( https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) policies for downlevel Windows and macOS.** These policies are deprecated in Microsoft Edge version 86 and will become obsolete in Microsoft Edge version 89.<br>
These policies are replaced by [Allow Telemetry](https://go.microsoft.com/fwlink/?linkid=2099569) on Windows 10, and the new [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) policy for all other platforms. This will let users manage the diagnostic data that gets sent to Microsoft for Windows 7, 8, 8.1 and macOS.

* **SameSite=Lax Cookies By Default**. To improve web security and privacy, cookies will now default to [SameSite=Lax](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie/SameSite) handling by default. This means that cookies will only be sent in a first-party context and will be omitted for requests sent to third-parties. This change can cause compatibility impact on websites that require cookies for third-party resources to function correctly. To permit such cookies, web developers can mark cookies which should be set from and sent to third-party contexts by adding explicit `SameSite=none` and `Secure` attributes when the cookie is set. Enterprises that wish to exempt certain sites from this change can do so using the [LegacySameSiteCookieBehaviorEnabledForDomainList](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabledfordomainlist) policy, or can opt-out of the change across all sites using the [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/deployedge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled) policy.

### Policy updates

#### New policies

Nineteen new policies were added. Download the updated Administrative Templates from the [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise). The following new policies were added.

- [CollectionsServicesAndExportsBlockList](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#collectionsservicesandexportsblocklist) - Block access to a specified list of services and export targets in Collections.
- [DefaultSensorsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsensorssetting) - Default sensors setting.
- [DefaultSerialGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultserialguardsetting) - Control use of the Serial API.
- [DiagnosticData](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#diagnosticdata) -  Send required and optional diagnostic data about browser usage.
- [EnterpriseModeSiteListManagerAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enterprisemodesitelistmanagerallowed) - Allow access to the Enterprise Mode Site List Manager tool.
- [ForceSync](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcesync) - Force synchronization of browser data and do not show the sync consent prompt.
- [InsecureFormsWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#insecureformswarningsenabled) - Enable warnings for insecure forms.
- [InternetExplorerIntegrationTestingAllowed](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationtestingallowed) - Allow Internet Explorer mode testing.
- [SpotlightExperiencesAndRecommendationsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#spotlightexperiencesandrecommendationsenabled) - Choose whether users can receive customized background images and text, suggestions, notifications, and tips for Microsoft services.
- [NewTabPageAllowedBackgroundTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpageallowedbackgroundtypes) - Configure the background types allowed for the new tab page layout.
- [SaveCookiesOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#savecookiesonexit) - Save cookies when Microsoft Edge closes.
- [SensorsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsallowedforurls) - Allow access to sensors on specific sites.
- [SensorsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sensorsblockedforurls) - Block access to sensors on specific sites.
- [SerialAskForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialaskforurls) - Allow the Serial API on specific sites.
- [SerialBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#serialblockedforurls) - Block the Serial API on specific sites.
- [URLBlocklist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlblocklist) - Block access to a list of URLs.
- [URLAllowlist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#urlallowlist) - Define a list of allowed URLs.
- [UserAgentClientHintsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#useragentclienthintsenabled) - Enable the User-Agent Client Hints feature.
- [UserDataSnapshotRetentionLimit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#userdatasnapshotretentionlimit) - Limits the number of user data snapshots retained for use in case of emergency rollback.

#### Deprecated Policies

- [MetricsReportingEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#metricsreportingenabled) - Enable usage and crash-related data reporting.
- [SendSiteInfoToImproveServices](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sendsiteinfotoimproveservices) - Send site information to improve Microsoft services.

#### Obsoleted Policy

[TLS13HardeningForLocalAnchorsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#tls13hardeningforlocalanchorsenabled) - Enable a TLS 1.3 security feature for local trust anchors.

#### Policy caption changed

[NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled) - Enable Native Window Occlusion.

#### Policy description changed

- [AdsSettingForIntrusiveAdsSites](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#adssettingforintrusiveadssites)
- [AllowTokenBindingForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#allowtokenbindingforurls)
- [AmbientAuthenticationInPrivateModesEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#ambientauthenticationinprivatemodesenabled)
- [ApplicationGuardContainerProxy](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#applicationguardcontainerproxy)
- [AutoImportAtFirstRun](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoimportatfirstrun)
- [AutoOpenFileTypes](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#autoopenfiletypes)
- [BrowserSignin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#browsersignin)
- [ClearBrowsingDataOnExit](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clearbrowsingdataonexit) 
- [ClickOnceEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#clickonceenabled)
- [CommandLineFlagSecurityWarningsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#commandlineflagsecuritywarningsenabled)
- [ConfigureOnPremisesAccountAutoSignIn](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureonpremisesaccountautosignin)
- [ConfigureShare](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#configureshare)
- [CookiesAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#cookiesallowedforurls)
- [CustomHelpLink](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#customhelplink)
- [DefaultCookiesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultcookiessetting)
- [DefaultGeolocationSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultgeolocationsetting)
- [DefaultImagesSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultimagessetting)
- [DefaultInsecureContentSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultinsecurecontentsetting)
- [DefaultJavaScriptSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultjavascriptsetting)
- [DefaultNotificationsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultnotificationssetting)
- [DefaultPluginsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpluginssetting)
- [DefaultPopupsSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultpopupssetting)
- [DefaultSearchProviderEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultsearchproviderenabled)
- [DefaultWebBluetoothGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebbluetoothguardsetting)
- [DefaultWebUsbGuardSetting](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#defaultwebusbguardsetting)
- [DelayNavigationsForInitialSiteListDownload](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#delaynavigationsforinitialsitelistdownload)
- [DeveloperToolsAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#developertoolsavailability)
- [EnableSha1ForLocalAnchors](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enablesha1forlocalanchors)
- [DownloadRestrictions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#downloadrestrictions)
- [EnableDeprecatedWebPlatformFeatures](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#enabledeprecatedwebplatformfeatures)
- [WinHttpProxyResolverEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#winhttpproxyresolverenabled)
- [ExperimentationAndConfigurationServiceControl](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#experimentationandconfigurationservicecontrol)
- [ExternalProtocolDialogShowAlwaysOpenCheckbox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#externalprotocoldialogshowalwaysopencheckbox)
- [ExtensionInstallForcelist](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#extensioninstallforcelist)
- [ForceBingSafeSearch](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forcebingsafesearch)
- [ForceYouTubeRestrict](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#forceyoutuberestrict)
- [HomepageIsNewTabPage](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepageisnewtabpage)
- [HomepageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#homepagelocation)
- [InPrivateModeAvailability](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#inprivatemodeavailability)
- [InternetExplorerIntegrationEnhancedHangDetection](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationenhancedhangdetection)
- [InternetExplorerIntegrationLevel](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationlevel)
- [InternetExplorerIntegrationSiteRedirect](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#internetexplorerintegrationsiteredirect)
- [LegacySameSiteCookieBehaviorEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#legacysamesitecookiebehaviorenabled)
- [NativeWindowOcclusionEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nativewindowocclusionenabled)
- [NavigationDelayForInitialSiteListDownloadTimeout](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#navigationdelayforinitialsitelistdownloadtimeout)
- [NetworkPredictionOptions](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#networkpredictionoptions)
- [NewTabPageLocation](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagelocation)
- [NewTabPageSearchBox](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesearchbox)
- [NewTabPageSetFeedType](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#newtabpagesetfeedtype)
- [NonRemovableProfileEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#nonremovableprofileenabled)
- [PasswordProtectionWarningTrigger](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionwarningtrigger)
- [PasswordProtectionLoginURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionloginurls)
- [PasswordProtectionChangePasswordURL](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#passwordprotectionchangepasswordurl)
- [PluginsAllowedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsallowedforurls)
- [PluginsBlockedForUrls](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#pluginsblockedforurls)
- [PreventSmartScreenPromptOverride](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverride)
- [PreventSmartScreenPromptOverrideForFiles](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#preventsmartscreenpromptoverrideforfiles)
- [ProxyMode](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#proxymode)
- [RegisteredProtocolHandlers](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#registeredprotocolhandlers)
- [RelaunchNotification](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#relaunchnotification)
- [RestoreOnStartup](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartup)
- [RestoreOnStartupURLs](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restoreonstartupurls)
- [RestrictSigninToPattern](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#restrictsignintopattern)
- [SSLVersionMin](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#sslversionmin)
- [SmartScreenAllowListDomains](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenallowlistdomains)
- [SmartScreenEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenenabled)
- [SmartScreenForTrustedDownloadsEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenfortrusteddownloadsenabled)
- [SmartScreenPuaEnabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#smartscreenpuaenabled)
- [SyncTypesListDisabled](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#synctypeslistdisabled)
- [TrackingPrevention](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#trackingprevention)
- [WebRtcLocalhostIpHandling](https://docs.microsoft.com/DeployEdge/microsoft-edge-policies#webrtclocalhostiphandling)

<!-- end 86 -->

## Version 85.0.564.41: August 25

Fixed various bugs and performance issues.

## Version 85.0.564.40: August 21

Fixed various bugs and performance issues.

## Version 85.0.564.36: August 17

Fixed various bugs and performance issues.

## Version 85.0.564.30: August 10

Fixed various bugs and performance issues.

## Version 85.0.564.23: August 3

Fixed various bugs and performance issues.

<!--- Archived to version 85.0.564.18: July 28 ---->

## See also

- [Microsoft Edge Enterprise landing page](https://aka.ms/EdgeEnterprise)
