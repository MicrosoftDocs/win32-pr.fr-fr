---
title: MDM_Policy_Result01_InternetExplorer02, classe
description: La \_ stratégie MDM \_ Result01 \_ InternetExplorer02 représente les stratégies Internet Explorer.
ms.assetid: 4b14c9ea-2f4d-4e5a-8aab-3741f15b0b1e
keywords:
- MDM_Policy_Result01_InternetExplorer02, classe
- Classe MDM_Policy_Result01_InternetExplorer02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_InternetExplorer02
- MDM_Policy_Result01_InternetExplorer02.InstanceID
- MDM_Policy_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63308b6100d6bd4ec924307a9dcd3892096fc0fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942015"
---
# <a name="mdm_policy_result01_internetexplorer02-class"></a><span data-ttu-id="40151-105">\_Classe InternetExplorer02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="40151-105">MDM\_Policy\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="40151-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="40151-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="40151-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="40151-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="40151-108">La \_ stratégie MDM \_ Result01 \_ InternetExplorer02 représente les stratégies Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="40151-108">The MDM\_Policy\_Result01\_InternetExplorer02 represents the Internet Explorer policies.</span></span>

<span data-ttu-id="40151-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="40151-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="40151-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40151-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="40151-111">Membres</span><span class="sxs-lookup"><span data-stu-id="40151-111">Members</span></span>

<span data-ttu-id="40151-112">La **classe \_ \_ Result01 \_ InternetExplorer02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="40151-112">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="40151-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40151-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="40151-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="40151-114">Properties</span></span>

<span data-ttu-id="40151-115">La **classe \_ \_ Result01 \_ InternetExplorer02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="40151-115">The **MDM\_Policy\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="40151-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="40151-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="40151-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="40151-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-125">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="40151-125">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-128">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="40151-128">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-131">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="40151-131">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-134">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="40151-134">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-137">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="40151-137">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-140">AllowFallbackToSSL3</span><span class="sxs-lookup"><span data-stu-id="40151-140">AllowFallbackToSSL3</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowfallbacktossl3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="40151-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="40151-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="40151-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="40151-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="40151-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="40151-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="40151-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="40151-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="40151-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-196">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="40151-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="40151-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="40151-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="40151-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="40151-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="40151-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="40151-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="40151-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="40151-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="40151-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="40151-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-236">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="40151-236">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-239">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="40151-239">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-242">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="40151-242">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-245">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="40151-245">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-248">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="40151-248">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-251">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="40151-251">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-254">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="40151-254">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-257">DisableUpdateCheck</span><span class="sxs-lookup"><span data-stu-id="40151-257">DisableUpdateCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableupdatecheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="40151-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-263">DoNotAllowUsersToAddSites</span><span class="sxs-lookup"><span data-stu-id="40151-263">DoNotAllowUsersToAddSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstoaddsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-266">DoNotAllowUsersToChangePolicies</span><span class="sxs-lookup"><span data-stu-id="40151-266">DoNotAllowUsersToChangePolicies</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowuserstochangepolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-269">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-269">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-271">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="40151-272">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-274">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-275">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="40151-275">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-277">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-278">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="40151-278">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-280">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-281">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="40151-281">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-283">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40151-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40151-284">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40151-284">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-285">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-285">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-287">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-288">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-290">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-291">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-293">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-294">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="40151-294">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-296">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="40151-297">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-299">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-300">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-300">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-302">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-303">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-303">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-305">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-306">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="40151-306">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-308">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-309">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-309">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-311">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-312">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-314">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="40151-315">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-317">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="40151-318">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-320">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-321">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="40151-321">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-323">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-324">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-324">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-326">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-327">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-327">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-329">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-330">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="40151-330">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-332">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-333">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-333">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-335">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-336">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-338">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-339">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-339">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-341">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-342">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-342">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-344">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-345">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="40151-345">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-347">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="40151-348">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-350">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="40151-351">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-353">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-354">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="40151-354">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-356">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-357">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="40151-357">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-359">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="40151-360">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-362">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-363">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-363">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-365">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-366">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-366">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-368">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="40151-369">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-370">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-371">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-372">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="40151-372">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-374">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-375">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-375">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-377">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="40151-378">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-380">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="40151-381">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-383">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="40151-384">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-386">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-387">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="40151-387">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-389">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="40151-390">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-392">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-393">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-393">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-395">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-396">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-398">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-399">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-401">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-402">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-402">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-404">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-405">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-405">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-407">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-408">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-408">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-409">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-410">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-411">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-411">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-413">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-414">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-414">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-416">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-417">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-417">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-419">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-420">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-422">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-423">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-423">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-425">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="40151-426">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-428">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-429">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-429">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-431">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-432">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-432">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-434">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-435">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-435">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-437">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-438">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-440">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-441">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-443">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-444">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-444">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-446">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-447">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-447">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-449">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-450">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-451">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-452">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-453">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-453">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-454">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-455">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-456">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-456">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-458">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-459">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-459">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-460">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-461">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-462">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-464">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-465">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-465">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-467">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-468">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-468">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-470">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-471">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-471">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-473">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-474">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-474">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-476">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-477">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-478">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-479">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-480">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-482">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-483">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-483">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-484">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-485">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-486">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-486">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-488">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-489">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-490">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-491">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-492">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-492">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-493">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-494">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-495">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-495">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-496">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-497">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-498">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-498">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-500">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-501">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-502">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-503">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-504">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-504">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-505">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-506">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-507">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-507">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-508">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-509">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-510">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-510">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-512">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-513">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-514">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-515">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-516">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-517">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-518">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-519">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-519">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-521">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-522">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-524">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-525">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-526">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-527">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-528">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-528">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-529">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-530">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-531">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-531">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-532">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-533">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-534">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-534">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-536">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-537">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-538">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-539">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-540">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-541">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-542">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-543">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-544">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-545">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-546">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-547">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-548">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-549">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-550">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-551">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-552">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-552">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-553">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-554">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-555">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-556">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-557">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-558">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-559">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-560">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-561">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-561">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-562">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-563">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-564">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-565">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-566">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-567">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-568">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-569">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-570">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-571">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-572">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-573">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-573">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-574">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-575">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-576">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-577">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-578">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-579">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-580">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-581">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-582">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-583">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-584">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-585">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-586">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-587">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-588">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-590">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-591">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-592">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-593">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-594">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-595">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-596">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-597">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-597">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-598">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-599">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-600">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-601">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-602">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-603">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-604">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-605">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-606">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-607">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-608">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-609">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-609">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-610">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-611">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-612">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-613">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-614">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-615">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-616">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-617">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-618">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-619">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-620">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-621">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-622">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-623">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-624">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-624">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-625">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-626">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-627">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-628">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-629">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-630">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-631">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-632">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-633">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-633">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-634">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-635">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-636">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-637">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-638">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-639">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-640">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-641">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-642">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-643">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-644">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-645">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-645">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-646">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-647">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-648">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-649">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-650">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-651">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-652">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-653">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-654">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-655">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-656">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-656">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-657">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-657">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-658">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-658">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-659">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-659">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-660">**ID**</span><span class="sxs-lookup"><span data-stu-id="40151-660">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-661">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-661">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-662">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="40151-662">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="40151-663">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="40151-663">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-664">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="40151-664">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-665">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-666">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-667">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-667">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-668">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-669">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-670">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-670">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-671">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-672">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-673">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-674">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-675">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-676">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-676">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-677">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-678">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-679">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-679">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-680">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-681">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-682">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="40151-682">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-683">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-684">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-685">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-686">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-687">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-688">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-689">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-690">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="40151-691">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-692">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-693">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-694">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="40151-694">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-695">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-696">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="40151-697">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-698">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-699">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-700">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-700">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-701">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-702">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-703">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-703">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-704">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-705">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-706">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-706">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-707">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-708">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="40151-709">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-710">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-711">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-712">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="40151-712">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-713">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-714">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-715">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-716">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-717">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-718">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-719">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-720">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="40151-721">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-722">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-723">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="40151-724">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-725">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-726">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="40151-727">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-728">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-729">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-730">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-730">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-731">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-732">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-733">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-733">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-734">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-735">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="40151-736">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-737">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-738">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-739">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-739">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-740">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-741">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-742">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-743">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-744">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-745">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-745">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-746">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-747">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-748">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-749">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-750">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="40151-751">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-752">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-753">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="40151-754">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-755">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-756">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="40151-757">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-758">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-759">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-760">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="40151-760">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-761">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-762">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="40151-763">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-764">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-765">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-766">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-767">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-768">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-769">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-769">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-770">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-771">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="40151-772">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-773">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-774">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-775">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="40151-775">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-776">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-777">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-778">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-778">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-779">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-780">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="40151-781">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-782">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-783">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="40151-784">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-785">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-786">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="40151-787">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-788">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-789">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="40151-790">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-791">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-792">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-793">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="40151-793">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-794">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-795">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="40151-796">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-797">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-798">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="40151-799">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-800">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-801">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-802">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="40151-802">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-803">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-804">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-805">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="40151-805">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-806">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-807">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-808">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-808">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-809">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-810">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="40151-811">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-812">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-813">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-814">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="40151-814">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-815">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-816">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-817">SecurityZonesUseOnlyMachineSettings</span><span class="sxs-lookup"><span data-stu-id="40151-817">SecurityZonesUseOnlyMachineSettings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-securityzonesuseonlymachinesettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-818">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-819">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-820">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="40151-820">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-821">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-822">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-823">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="40151-823">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-824">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-825">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-826">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-827">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-828">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-829">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-830">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-831">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-832">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="40151-832">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-833">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-834">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-835">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="40151-835">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-836">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-837">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="40151-838">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-839">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-840">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-841">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="40151-841">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-842">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-843">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-844">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="40151-844">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-845">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-846">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-847">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="40151-847">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-848">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-849">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-850">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-851">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-852">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-853">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-854">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-855">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="40151-856">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-857">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-858">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="40151-859">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-860">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-861">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="40151-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="40151-862">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-863">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-863">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-864">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-864">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-865">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="40151-865">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-866">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-866">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-867">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-867">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="40151-868">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="40151-868">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="40151-869">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="40151-869">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40151-870">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="40151-870">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="40151-871">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40151-871">Requirements</span></span>



| <span data-ttu-id="40151-872">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40151-872">Requirement</span></span> | <span data-ttu-id="40151-873">Valeur</span><span class="sxs-lookup"><span data-stu-id="40151-873">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40151-874">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40151-874">Minimum supported client</span></span><br/> | <span data-ttu-id="40151-875">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40151-875">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40151-876">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40151-876">Minimum supported server</span></span><br/> | <span data-ttu-id="40151-877">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="40151-877">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="40151-878">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="40151-878">Namespace</span></span><br/>                | <span data-ttu-id="40151-879">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="40151-879">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="40151-880">MOF</span><span class="sxs-lookup"><span data-stu-id="40151-880">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40151-881"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40151-881"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="40151-882">DLL</span><span class="sxs-lookup"><span data-stu-id="40151-882">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40151-883"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40151-883"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

