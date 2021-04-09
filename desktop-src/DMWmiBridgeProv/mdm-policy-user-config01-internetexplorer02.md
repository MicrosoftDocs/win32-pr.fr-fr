---
title: MDM_Policy_User_Config01_InternetExplorer02, classe
description: La \_ \_ classe Config01 InternetExplorer02 utilisateur de la stratégie MDM \_ \_ représente les stratégies Internet Explorer disponibles.
ms.assetid: 2b155e65-5a81-4916-815f-23763759bb9a
keywords:
- MDM_Policy_User_Config01_InternetExplorer02, classe
- Classe MDM_Policy_User_Config01_InternetExplorer02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_InternetExplorer02
- MDM_Policy_User_Config01_InternetExplorer02.InstanceID
- MDM_Policy_User_Config01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2f79c00505037508307e93120f9e2545b135678
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032908"
---
# <a name="mdm_policy_user_config01_internetexplorer02-class"></a><span data-ttu-id="f11b3-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Config01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="f11b3-105">MDM\_Policy\_User\_Config01\_InternetExplorer02 class</span></span>

<span data-ttu-id="f11b3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="f11b3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f11b3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="f11b3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f11b3-108">La \_ \_ classe Config01 InternetExplorer02 utilisateur de la stratégie MDM \_ \_ représente les stratégies Internet Explorer disponibles.</span><span class="sxs-lookup"><span data-stu-id="f11b3-108">The MDM\_Policy\_User\_Config01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="f11b3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f11b3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11b3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f11b3-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_InternetExplorer02
{
  string InstanceID;
  string ParentID;
  string AddSearchProvider;
  string AllowActiveXFiltering;
  string AllowAddOnList;
  string AllowDeletingBrowsingHistoryOnExit;
  string AllowCertificateAddressMismatchWarning;
  string AllowAutoComplete;
  string AllowEnhancedProtectedMode;
  string AllowEnterpriseModeFromToolsMenu;
  string AllowEnterpriseModeSiteList;
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
  string DisableHomePageChange;
  string DisableProcessesInEnhancedProtectedMode;
  string DisableInPrivateBrowsing;
  string DisableIgnoringCertificateErrors;
  string DisableProxyChange;
  string DisableSearchProviderChange;
  string DisableSecondaryHomePageChange;
  string DoNotAllowActiveXControlsInProtectedMode;
  string DisableSecuritySettingsCheck;
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

## <a name="members"></a><span data-ttu-id="f11b3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="f11b3-111">Members</span></span>

<span data-ttu-id="f11b3-112">La **classe \_ \_ \_ Config01 \_ InternetExplorer02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f11b3-112">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="f11b3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f11b3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f11b3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f11b3-114">Properties</span></span>

<span data-ttu-id="f11b3-115">La **classe \_ \_ \_ Config01 \_ InternetExplorer02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f11b3-115">The **MDM\_Policy\_User\_Config01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f11b3-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="f11b3-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="f11b3-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="f11b3-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="f11b3-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="f11b3-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="f11b3-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f11b3-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="f11b3-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="f11b3-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="f11b3-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="f11b3-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="f11b3-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="f11b3-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="f11b3-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="f11b3-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="f11b3-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="f11b3-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-196">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="f11b3-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="f11b3-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="f11b3-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="f11b3-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="f11b3-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="f11b3-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="f11b3-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="f11b3-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="f11b3-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="f11b3-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="f11b3-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="f11b3-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="f11b3-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f11b3-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="f11b3-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="f11b3-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="f11b3-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="f11b3-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f11b3-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="f11b3-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-271">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="f11b3-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-274">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f11b3-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f11b3-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-278">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f11b3-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-281">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-283">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-284">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-287">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="f11b3-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-290">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-293">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-296">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-299">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-302">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-305">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-308">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="f11b3-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-311">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-314">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="f11b3-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-317">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-320">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-323">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="f11b3-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-326">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-329">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-332">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-335">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-338">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="f11b3-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-341">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="f11b3-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-344">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="f11b3-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-347">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="f11b3-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-350">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f11b3-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-353">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="f11b3-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-356">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-359">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-362">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="f11b3-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-365">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="f11b3-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-368">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-370">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-371">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="f11b3-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-374">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="f11b3-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-377">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-380">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="f11b3-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-383">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="f11b3-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-386">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-389">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-392">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-395">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-398">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-401">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-404">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-407">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-409">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-410">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-413">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-416">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-419">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="f11b3-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-422">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-425">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-428">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-431">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-434">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-437">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-440">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-443">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-446">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-449">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-451">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-452">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-454">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-455">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-458">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-460">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-461">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-464">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-467">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-470">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-473">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-476">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-478">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-479">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-482">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-484">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-485">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-488">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-490">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-491">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-493">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-494">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-496">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-497">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-500">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-502">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-503">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-505">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-506">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-508">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-509">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-512">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-514">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-515">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-517">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-518">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-521">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-524">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-526">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-527">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-529">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-530">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-532">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-533">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-536">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-538">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-539">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-541">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-542">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-544">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-545">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-547">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-548">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-550">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-551">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-553">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-554">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-556">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-557">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-559">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-560">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-562">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-563">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-565">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-566">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-568">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-569">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-571">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-572">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-574">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-575">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-577">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-578">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-580">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-581">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-583">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-584">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-586">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-587">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-590">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-592">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-593">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-595">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-596">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-598">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-599">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-601">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-602">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-604">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-605">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-607">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-608">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-610">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-611">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-613">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-614">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-616">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-617">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-619">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-620">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-622">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-623">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-625">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-626">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-628">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-629">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-631">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-632">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-634">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-635">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-637">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-638">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-640">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-641">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-643">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-644">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-646">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-647">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-649">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-650">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-652">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-653">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-654">**ID**</span><span class="sxs-lookup"><span data-stu-id="f11b3-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-655">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-656">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f11b3-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-657">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f11b3-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="f11b3-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-659">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-660">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-662">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-663">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-665">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-666">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-668">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-669">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-671">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-672">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-674">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-675">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="f11b3-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-677">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-678">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-680">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-681">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-683">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-684">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="f11b3-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-686">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-687">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="f11b3-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-689">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-690">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-692">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-693">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-695">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-696">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-698">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-699">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-701">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-702">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-704">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-705">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="f11b3-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-707">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-708">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-710">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-711">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-713">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-714">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="f11b3-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-716">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-717">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-719">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-720">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="f11b3-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-722">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-723">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-725">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-726">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-728">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-729">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="f11b3-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-731">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-732">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-734">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-735">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-737">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-738">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-740">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-741">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-743">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-744">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="f11b3-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-746">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-747">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="f11b3-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-749">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-750">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="f11b3-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-752">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-753">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="f11b3-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-755">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-756">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="f11b3-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-758">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-759">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-761">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-762">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-764">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-765">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="f11b3-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-767">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-768">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="f11b3-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-770">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-771">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-773">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-774">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="f11b3-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-776">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-777">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="f11b3-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-779">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-780">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="f11b3-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-782">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-783">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="f11b3-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-785">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-786">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="f11b3-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-788">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-789">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="f11b3-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-791">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-792">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="f11b3-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-794">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-795">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="f11b3-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-797">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-798">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="f11b3-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-800">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-801">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-803">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-804">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="f11b3-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-806">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-807">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="f11b3-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-809">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-810">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="f11b3-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-812">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-813">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="f11b3-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-815">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-816">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-818">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-819">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-821">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-822">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="f11b3-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-824">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-825">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="f11b3-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-827">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-828">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="f11b3-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-830">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-831">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="f11b3-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-833">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-834">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="f11b3-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-836">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-837">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="f11b3-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-839">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-840">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-842">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-843">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-845">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-846">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="f11b3-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-848">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-849">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="f11b3-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-851">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-852">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f11b3-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="f11b3-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-854">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-855">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="f11b3-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-857">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-858">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f11b3-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="f11b3-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11b3-860">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f11b3-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11b3-861">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="f11b3-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f11b3-862">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f11b3-862">Requirements</span></span>



| <span data-ttu-id="f11b3-863">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f11b3-863">Requirement</span></span> | <span data-ttu-id="f11b3-864">Valeur</span><span class="sxs-lookup"><span data-stu-id="f11b3-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f11b3-865">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f11b3-865">Minimum supported client</span></span><br/> | <span data-ttu-id="f11b3-866">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f11b3-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f11b3-867">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f11b3-867">Minimum supported server</span></span><br/> | <span data-ttu-id="f11b3-868">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f11b3-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f11b3-869">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f11b3-869">Namespace</span></span><br/>                | <span data-ttu-id="f11b3-870">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="f11b3-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f11b3-871">MOF</span><span class="sxs-lookup"><span data-stu-id="f11b3-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f11b3-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f11b3-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f11b3-873">DLL</span><span class="sxs-lookup"><span data-stu-id="f11b3-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f11b3-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f11b3-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

