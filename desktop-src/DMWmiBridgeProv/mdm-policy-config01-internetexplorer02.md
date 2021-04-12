---
title: MDM_Policy_Config01_InternetExplorer02, classe
description: La \_ classe Config01 InternetExplorer02 de la stratégie MDM \_ \_ configure les stratégies Internet Explorer.
ms.assetid: 32cc6a64-3008-4add-96e8-33b31beb207f
keywords:
- MDM_Policy_Config01_InternetExplorer02, classe
- Classe MDM_Policy_Config01_InternetExplorer02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_InternetExplorer02
- MDM_Policy_Config01_InternetExplorer02.InstanceID
- MDM_Policy_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a448b0034e3f4658f1c13b238abf455bf413a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465242"
---
# <a name="mdm_policy_config01_internetexplorer02-class"></a><span data-ttu-id="33f2a-105">\_Classe InternetExplorer02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="33f2a-105">MDM\_Policy\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="33f2a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="33f2a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33f2a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="33f2a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33f2a-108">La \_ classe Config01 InternetExplorer02 de la stratégie MDM \_ \_ configure les stratégies Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="33f2a-108">The MDM\_Policy\_Config01\_InternetExplorer02 class configures the Internet Explorer policies.</span></span>

<span data-ttu-id="33f2a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="33f2a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33f2a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33f2a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
  string AllowFallbackToSSL3;
  string AllowInternetExplorer7PolicyList;
  string AllowInternetExplorerStandardsMode;
  string AllowInternetZoneTemplate;
  string AllowIntranetZoneTemplate;
  string AllowLocalMachineZoneTemplate;
  string AllowLockedDownInternetZoneTemplate;
  string AllowLockedDownIntranetZoneTemplate;
  string AllowLockedDownLocalMachineZoneTemplate;
  string AllowLockedDownRestrictedSitesZoneTemplate;
  string AllowOneWordEntry;
  string AllowSiteToZoneAssignmentList;
  string AllowsLockedDownTrustedSitesZoneTemplate;
  string AllowSoftwareWhenSignatureIsInvalid;
  string AllowsRestrictedSitesZoneTemplate;
  string AllowSuggestedSites;
  string AllowTrustedSitesZoneTemplate;
  string ConsistentMimeHandlingInternetExplorerProcesses;
  string CheckSignaturesOnDownloadedPrograms;
  string CheckServerCertificateRevocation;
  string DisableAdobeFlash;
  string DisableBlockingOfOutdatedActiveXControls;
  string DisableBypassOfSmartScreenWarnings;
  string DisableBypassOfSmartScreenWarningsAboutUncommonFiles;
  string DisableCrashDetection;
  string DisableConfiguringHistory;
  string DisableCustomerExperienceImprovementProgramParticipation;
  string DisableDeletingUserVisitedWebsites;
  string DisableEnclosureDownloading;
  string DisableEncryptionSupport;
  string DisableFirstRunWizard;
  string DisableFlipAheadFeature;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DisableSecuritySettingsCheck;
  string DisableUpdateCheck;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DoNotAllowUsersToAddSites;
  string DoNotAllowUsersToChangePolicies;
  string DoNotBlockOutdatedActiveXControls;
  string DoNotBlockOutdatedActiveXControlsOnSpecificDomains;
  string IncludeAllLocalSites;
  string IncludeAllNetworkPaths;
  string InternetZoneAllowAccessToDataSources;
  string InternetZoneAllowAutomaticPromptingForActiveXControls;
  string InternetZoneAllowAutomaticPromptingForFileDownloads;
  string InternetZoneAllowDragAndDropCopyAndPasteFiles;
  string InternetZoneAllowCopyPasteViaScript;
  string InternetZoneAllowFontDownloads;
  string InternetZoneAllowLessPrivilegedSites;
  string InternetZoneAllowLoadingOfXAMLFiles;
  string InternetZoneAllowNETFrameworkReliantComponents;
  string InternetZoneAllowScriptInitiatedWindows;
  string InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string InternetZoneAllowScriptlets;
  string InternetZoneAllowSmartScreenIE;
  string InternetZoneAllowUpdatesToStatusBarViaScript;
  string InternetZoneAllowUserDataPersistence;
  string InternetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string InternetZoneIncludeLocalPathWhenUploadingFilesToServer;
  string InternetZoneEnableProtectedMode;
  string InternetZoneEnableMIMESniffing;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string InternetZoneEnableCrossSiteScriptingFilter;
  string InternetZoneDownloadUnsignedActiveXControls;
  string InternetZoneDownloadSignedActiveXControls;
  string InternetZoneInitializeAndScriptActiveXControls;
  string InternetZoneJavaPermissions;
  string InternetZoneLogonOptions;
  string InternetZoneLaunchingApplicationsAndFilesInIFRAME;
  string InternetZoneNavigateWindowsAndFrames;
  string InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone;
  string InternetZoneUsePopupBlocker;
  string InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode;
  string IntranetZoneAllowAccessToDataSources;
  string IntranetZoneAllowAutomaticPromptingForActiveXControls;
  string IntranetZoneAllowAutomaticPromptingForFileDownloads;
  string IntranetZoneAllowFontDownloads;
  string IntranetZoneAllowLessPrivilegedSites;
  string IntranetZoneAllowNETFrameworkReliantComponents;
  string IntranetZoneAllowScriptlets;
  string IntranetZoneAllowSmartScreenIE;
  string IntranetZoneAllowUserDataPersistence;
  string IntranetZoneDoNotRunAntimalwareAgainstActiveXControls;
  string IntranetZoneInitializeAndScriptActiveXControls;
  string IntranetZoneJavaPermissions;
  string IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string IntranetZoneNavigateWindowsAndFrames;
  string LocalMachineZoneAllowAccessToDataSources;
  string LocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LocalMachineZoneAllowFontDownloads;
  string LocalMachineZoneAllowLessPrivilegedSites;
  string LocalMachineZoneAllowNETFrameworkReliantComponents;
  string LocalMachineZoneAllowScriptlets;
  string LocalMachineZoneAllowSmartScreenIE;
  string LocalMachineZoneAllowUserDataPersistence;
  string LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls;
  string LocalMachineZoneInitializeAndScriptActiveXControls;
  string LocalMachineZoneJavaPermissions;
  string LocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownInternetZoneAllowAccessToDataSources;
  string LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownInternetZoneAllowFontDownloads;
  string LockedDownInternetZoneAllowLessPrivilegedSites;
  string LockedDownInternetZoneAllowNETFrameworkReliantComponents;
  string LockedDownInternetZoneAllowScriptlets;
  string LockedDownInternetZoneAllowSmartScreenIE;
  string LockedDownInternetZoneAllowUserDataPersistence;
  string LockedDownInternetZoneInitializeAndScriptActiveXControls;
  string LockedDownInternetZoneJavaPermissions;
  string LockedDownInternetZoneNavigateWindowsAndFrames;
  string LockedDownIntranetZoneAllowAccessToDataSources;
  string LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownIntranetZoneAllowFontDownloads;
  string LockedDownIntranetZoneAllowLessPrivilegedSites;
  string LockedDownIntranetZoneAllowNETFrameworkReliantComponents;
  string LockedDownIntranetZoneAllowScriptlets;
  string LockedDownIntranetZoneAllowSmartScreenIE;
  string LockedDownIntranetZoneAllowUserDataPersistence;
  string LockedDownIntranetZoneInitializeAndScriptActiveXControls;
  string LockedDownIntranetZoneNavigateWindowsAndFrames;
  string LockedDownLocalMachineZoneAllowAccessToDataSources;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownLocalMachineZoneAllowFontDownloads;
  string LockedDownLocalMachineZoneAllowLessPrivilegedSites;
  string LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents;
  string LockedDownLocalMachineZoneAllowScriptlets;
  string LockedDownLocalMachineZoneAllowSmartScreenIE;
  string LockedDownLocalMachineZoneAllowUserDataPersistence;
  string LockedDownLocalMachineZoneInitializeAndScriptActiveXControls;
  string LockedDownLocalMachineZoneJavaPermissions;
  string LockedDownLocalMachineZoneNavigateWindowsAndFrames;
  string LockedDownRestrictedSitesZoneAllowAccessToDataSources;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownRestrictedSitesZoneAllowFontDownloads;
  string LockedDownRestrictedSitesZoneAllowLessPrivilegedSites;
  string LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownRestrictedSitesZoneAllowScriptlets;
  string LockedDownRestrictedSitesZoneAllowSmartScreenIE;
  string LockedDownRestrictedSitesZoneAllowUserDataPersistence;
  string LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownRestrictedSitesZoneJavaPermissions;
  string LockedDownRestrictedSitesZoneNavigateWindowsAndFrames;
  string LockedDownTrustedSitesZoneAllowAccessToDataSources;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string LockedDownTrustedSitesZoneAllowFontDownloads;
  string LockedDownTrustedSitesZoneAllowLessPrivilegedSites;
  string LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents;
  string LockedDownTrustedSitesZoneAllowScriptlets;
  string LockedDownTrustedSitesZoneAllowSmartScreenIE;
  string LockedDownTrustedSitesZoneAllowUserDataPersistence;
  string LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls;
  string LockedDownTrustedSitesZoneJavaPermissions;
  string LockedDownTrustedSitesZoneNavigateWindowsAndFrames;
  string RestrictActiveXInstallInternetExplorerProcesses;
  string RemoveRunThisTimeButtonForOutdatedActiveXControls;
  string ProtectionFromZoneElevationInternetExplorerProcesses;
  string PreventPerUserInstallationOfActiveXControls;
  string PreventManagingSmartScreenFilter;
  string NotificationBarInternetExplorerProcesses;
  string MKProtocolSecurityRestrictionInternetExplorerProcesses;
  string MimeSniffingSafetyFeatureInternetExplorerProcesses;
  string RestrictedSitesZoneAllowAccessToDataSources;
  string RestrictedSitesZoneAllowActiveScripting;
  string RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string RestrictedSitesZoneAllowFileDownloads;
  string RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles;
  string RestrictedSitesZoneAllowCopyPasteViaScript;
  string RestrictedSitesZoneAllowBinaryAndScriptBehaviors;
  string RestrictedSitesZoneAllowFontDownloads;
  string RestrictedSitesZoneAllowLessPrivilegedSites;
  string RestrictedSitesZoneAllowMETAREFRESH;
  string RestrictedSitesZoneAllowLoadingOfXAMLFiles;
  string RestrictedSitesZoneAllowNETFrameworkReliantComponents;
  string RestrictedSitesZoneAllowScriptInitiatedWindows;
  string RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl;
  string RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls;
  string RestrictedSitesZoneAllowScriptlets;
  string RestrictedSitesZoneAllowSmartScreenIE;
  string RestrictedSitesZoneAllowUpdatesToStatusBarViaScript;
  string RestrictedSitesZoneAllowUserDataPersistence;
  string RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer;
  string RestrictedSitesZoneEnableMIMESniffing;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows;
  string RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows;
  string RestrictedSitesZoneDownloadUnsignedActiveXControls;
  string RestrictedSitesZoneEnableCrossSiteScriptingFilter;
  string RestrictedSitesZoneDownloadSignedActiveXControls;
  string RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string RestrictedSitesZoneInitializeAndScriptActiveXControls;
  string RestrictedSitesZoneLogonOptions;
  string RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME;
  string RestrictedSitesZoneJavaPermissions;
  string RestrictedSitesZoneNavigateWindowsAndFrames;
  string ScriptedWindowSecurityRestrictionsInternetExplorerProcesses;
  string RestrictFileDownloadInternetExplorerProcesses;
  string RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting;
  string RestrictedSitesZoneUsePopupBlocker;
  string RestrictedSitesZoneTurnOnProtectedMode;
  string RestrictedSitesZoneTurnOnCrossSiteScriptingFilter;
  string RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles;
  string RestrictedSitesZoneScriptingOfJavaApplets;
  string RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode;
  string RestrictedSitesZoneRunActiveXControlsAndPlugins;
  string RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains;
  string SearchProviderList;
  string SpecifyUseOfActiveXInstallerService;
  string SecurityZonesUseOnlyMachineSettings;
  string TrustedSitesZoneAllowAccessToDataSources;
  string TrustedSitesZoneAllowAutomaticPromptingForActiveXControls;
  string TrustedSitesZoneAllowAutomaticPromptingForFileDownloads;
  string TrustedSitesZoneAllowFontDownloads;
  string TrustedSitesZoneAllowLessPrivilegedSites;
  string TrustedSitesZoneAllowNETFrameworkReliantComponents;
  string TrustedSitesZoneAllowScriptlets;
  string TrustedSitesZoneAllowSmartScreenIE;
  string TrustedSitesZoneAllowUserDataPersistence;
  string TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls;
  string TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControls;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe;
  string TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe;
  string TrustedSitesZoneJavaPermissions;
  string TrustedSitesZoneNavigateWindowsAndFrames;
};
```

## <a name="members"></a><span data-ttu-id="33f2a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="33f2a-111">Members</span></span>

<span data-ttu-id="33f2a-112">La **classe \_ \_ Config01 \_ InternetExplorer02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="33f2a-112">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="33f2a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33f2a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33f2a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="33f2a-114">Properties</span></span>

<span data-ttu-id="33f2a-115">La **classe \_ \_ Config01 \_ InternetExplorer02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="33f2a-115">The **MDM\_Policy\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33f2a-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="33f2a-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="33f2a-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="33f2a-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="33f2a-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="33f2a-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="33f2a-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="33f2a-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="33f2a-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="33f2a-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="33f2a-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="33f2a-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="33f2a-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="33f2a-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="33f2a-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="33f2a-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="33f2a-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="33f2a-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-196">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="33f2a-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="33f2a-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="33f2a-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="33f2a-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="33f2a-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="33f2a-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="33f2a-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="33f2a-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="33f2a-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="33f2a-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="33f2a-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="33f2a-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="33f2a-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="33f2a-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="33f2a-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="33f2a-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="33f2a-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="33f2a-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="33f2a-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="33f2a-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-271">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="33f2a-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-274">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-277">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="33f2a-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-280">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33f2a-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33f2a-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-284">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33f2a-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-287">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-290">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-293">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="33f2a-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-296">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-299">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-302">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-305">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-308">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-311">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-314">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="33f2a-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-317">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-320">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="33f2a-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-323">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-326">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-329">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="33f2a-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-332">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-335">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-338">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-341">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-344">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="33f2a-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-347">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="33f2a-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-350">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="33f2a-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-353">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="33f2a-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-356">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="33f2a-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-359">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="33f2a-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-362">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-365">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-368">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="33f2a-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-370">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-371">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="33f2a-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-374">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-377">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="33f2a-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-380">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="33f2a-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-383">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-386">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="33f2a-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-389">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="33f2a-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-392">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-395">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-398">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-401">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-404">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-407">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-409">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-410">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-413">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-416">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-419">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-422">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-425">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="33f2a-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-428">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-431">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-434">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-437">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-440">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-443">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-446">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-449">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-451">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-452">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-454">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-455">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-458">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-460">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-461">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-464">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-467">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-470">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-473">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-476">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-478">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-479">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-482">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-484">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-485">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-488">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-490">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-491">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-493">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-494">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-496">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-497">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-500">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-502">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-503">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-505">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-506">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-508">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-509">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-512">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-514">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-515">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-517">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-518">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-521">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-524">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-526">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-527">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-529">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-530">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-532">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-533">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-536">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-538">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-539">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-541">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-542">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-544">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-545">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-547">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-548">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-550">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-551">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-553">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-554">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-556">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-557">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-559">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-560">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-562">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-563">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-565">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-566">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-568">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-569">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-571">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-572">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-574">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-575">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-577">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-578">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-580">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-581">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-583">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-584">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-586">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-587">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-590">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-592">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-593">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-595">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-596">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-598">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-599">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-601">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-602">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-604">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-605">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-607">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-608">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-610">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-611">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-613">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-614">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-616">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-617">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-619">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-620">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-622">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-623">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-625">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-626">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-628">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-629">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-631">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-632">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-634">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-635">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-637">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-638">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-640">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-641">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-643">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-644">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-646">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-647">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-649">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-650">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-652">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-653">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-655">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-656">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-658">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-659">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-660">**ID**</span><span class="sxs-lookup"><span data-stu-id="33f2a-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-661">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-662">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="33f2a-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-663">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33f2a-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="33f2a-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-665">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-666">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-668">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-669">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-671">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-672">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-674">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-675">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-677">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-678">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-680">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-681">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="33f2a-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-683">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-684">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-686">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-687">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-689">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-690">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="33f2a-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-692">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-693">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="33f2a-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-695">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-696">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-698">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-699">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-701">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-702">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-704">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-705">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-707">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-708">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-710">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-711">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="33f2a-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-713">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-714">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-716">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-717">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-719">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-720">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="33f2a-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-722">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-723">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-725">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-726">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="33f2a-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-728">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-729">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-731">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-732">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-734">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-735">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="33f2a-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-737">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-738">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-740">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-741">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-743">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-744">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-746">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-747">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-749">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-750">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="33f2a-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-752">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-753">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="33f2a-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-755">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-756">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="33f2a-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-758">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-759">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="33f2a-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-761">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-762">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="33f2a-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-764">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-765">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-767">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-768">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-770">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-771">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="33f2a-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-773">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-774">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="33f2a-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-776">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-777">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-779">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-780">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="33f2a-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-782">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-783">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="33f2a-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-785">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-786">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="33f2a-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-788">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-789">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="33f2a-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-791">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-792">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="33f2a-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-794">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-795">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="33f2a-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-797">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-798">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="33f2a-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-800">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-801">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="33f2a-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-803">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-804">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="33f2a-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-806">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-807">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-809">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-810">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="33f2a-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-812">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-813">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="33f2a-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-815">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-816">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="33f2a-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-818">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-819">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="33f2a-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-821">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-822">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="33f2a-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-824">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-825">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-827">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-828">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-830">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-831">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="33f2a-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-833">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-834">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="33f2a-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-836">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-837">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="33f2a-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-839">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-840">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="33f2a-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-842">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-843">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="33f2a-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-845">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-846">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="33f2a-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-848">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-849">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-851">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-852">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-854">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-855">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="33f2a-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-857">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-858">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="33f2a-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-860">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-861">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33f2a-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="33f2a-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-863">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-864">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="33f2a-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-866">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-867">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="33f2a-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="33f2a-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33f2a-869">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="33f2a-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33f2a-870">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="33f2a-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33f2a-871">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33f2a-871">Requirements</span></span>



| <span data-ttu-id="33f2a-872">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33f2a-872">Requirement</span></span> | <span data-ttu-id="33f2a-873">Valeur</span><span class="sxs-lookup"><span data-stu-id="33f2a-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33f2a-874">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f2a-874">Minimum supported client</span></span><br/> | <span data-ttu-id="33f2a-875">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="33f2a-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33f2a-876">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f2a-876">Minimum supported server</span></span><br/> | <span data-ttu-id="33f2a-877">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="33f2a-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="33f2a-878">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="33f2a-878">Namespace</span></span><br/>                | <span data-ttu-id="33f2a-879">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="33f2a-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="33f2a-880">MOF</span><span class="sxs-lookup"><span data-stu-id="33f2a-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33f2a-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33f2a-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="33f2a-882">DLL</span><span class="sxs-lookup"><span data-stu-id="33f2a-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33f2a-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33f2a-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

