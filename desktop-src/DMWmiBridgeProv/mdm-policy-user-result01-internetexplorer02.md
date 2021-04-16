---
title: MDM_Policy_User_Result01_InternetExplorer02, classe
description: La \_ \_ classe Result01 InternetExplorer02 utilisateur de la stratégie MDM \_ \_ représente les stratégies Internet Explorer disponibles.
ms.assetid: efd999aa-4aa8-486d-82d4-20af7e2005fe
keywords:
- MDM_Policy_User_Result01_InternetExplorer02, classe
- Classe MDM_Policy_User_Result01_InternetExplorer02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_InternetExplorer02
- MDM_Policy_User_Result01_InternetExplorer02.InstanceID
- MDM_Policy_User_Result01_InternetExplorer02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8693720c7a973cc6bc689abbf76a4674f185e23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464370"
---
# <a name="mdm_policy_user_result01_internetexplorer02-class"></a><span data-ttu-id="0ad46-105">Classe d’utilisateur de la \_ stratégie MDM \_ \_ Result01 \_ InternetExplorer02</span><span class="sxs-lookup"><span data-stu-id="0ad46-105">MDM\_Policy\_User\_Result01\_InternetExplorer02 class</span></span>

<span data-ttu-id="0ad46-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="0ad46-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0ad46-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="0ad46-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0ad46-108">La \_ \_ classe Result01 InternetExplorer02 utilisateur de la stratégie MDM \_ \_ représente les stratégies Internet Explorer disponibles.</span><span class="sxs-lookup"><span data-stu-id="0ad46-108">The MDM\_Policy\_User\_Result01\_InternetExplorer02 class represents the available Internet Explorer policies.</span></span>

<span data-ttu-id="0ad46-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="0ad46-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ad46-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ad46-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_InternetExplorer02
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

## <a name="members"></a><span data-ttu-id="0ad46-111">Membres</span><span class="sxs-lookup"><span data-stu-id="0ad46-111">Members</span></span>

<span data-ttu-id="0ad46-112">La **classe \_ \_ \_ Result01 \_ InternetExplorer02 de la stratégie MDM User** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0ad46-112">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these types of members:</span></span>

-   [<span data-ttu-id="0ad46-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ad46-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0ad46-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0ad46-114">Properties</span></span>

<span data-ttu-id="0ad46-115">La **classe \_ \_ \_ Result01 \_ InternetExplorer02 de la stratégie MDM User** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0ad46-115">The **MDM\_Policy\_User\_Result01\_InternetExplorer02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0ad46-116">AddSearchProvider</span><span class="sxs-lookup"><span data-stu-id="0ad46-116">AddSearchProvider</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-addsearchprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-119">AllowActiveXFiltering</span><span class="sxs-lookup"><span data-stu-id="0ad46-119">AllowActiveXFiltering</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowactivexfiltering)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-122">AllowAddOnList</span><span class="sxs-lookup"><span data-stu-id="0ad46-122">AllowAddOnList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowaddonlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-125">AllowAutoComplete</span><span class="sxs-lookup"><span data-stu-id="0ad46-125">AllowAutoComplete</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowautocomplete)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-128">AllowCertificateAddressMismatchWarning</span><span class="sxs-lookup"><span data-stu-id="0ad46-128">AllowCertificateAddressMismatchWarning</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowcertificateaddressmismatchwarning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-131">AllowDeletingBrowsingHistoryOnExit</span><span class="sxs-lookup"><span data-stu-id="0ad46-131">AllowDeletingBrowsingHistoryOnExit</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowdeletingbrowsinghistoryonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-134">AllowEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0ad46-134">AllowEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-137">AllowEnterpriseModeFromToolsMenu</span><span class="sxs-lookup"><span data-stu-id="0ad46-137">AllowEnterpriseModeFromToolsMenu</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodefromtoolsmenu)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-140">AllowEnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="0ad46-140">AllowEnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowenterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-143">AllowInternetExplorer7PolicyList</span><span class="sxs-lookup"><span data-stu-id="0ad46-143">AllowInternetExplorer7PolicyList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorer7policylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-146">AllowInternetExplorerStandardsMode</span><span class="sxs-lookup"><span data-stu-id="0ad46-146">AllowInternetExplorerStandardsMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetexplorerstandardsmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-149">AllowInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-149">AllowInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowinternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-152">AllowIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-152">AllowIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-155">AllowLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-155">AllowLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-158">AllowLockedDownInternetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-158">AllowLockedDownInternetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddowninternetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-161">AllowLockedDownIntranetZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-161">AllowLockedDownIntranetZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownintranetzonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-164">AllowLockedDownLocalMachineZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-164">AllowLockedDownLocalMachineZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownlocalmachinezonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-167">AllowLockedDownRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-167">AllowLockedDownRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowlockeddownrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-170">AllowOneWordEntry</span><span class="sxs-lookup"><span data-stu-id="0ad46-170">AllowOneWordEntry</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowonewordentry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-171">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-173">AllowSiteToZoneAssignmentList</span><span class="sxs-lookup"><span data-stu-id="0ad46-173">AllowSiteToZoneAssignmentList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsitetozoneassignmentlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-176">AllowsLockedDownTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-176">AllowsLockedDownTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowslockeddowntrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-179">AllowSoftwareWhenSignatureIsInvalid</span><span class="sxs-lookup"><span data-stu-id="0ad46-179">AllowSoftwareWhenSignatureIsInvalid</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsoftwarewhensignatureisinvalid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-182">AllowsRestrictedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-182">AllowsRestrictedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsrestrictedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-185">AllowSuggestedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-185">AllowSuggestedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowsuggestedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-188">AllowTrustedSitesZoneTemplate</span><span class="sxs-lookup"><span data-stu-id="0ad46-188">AllowTrustedSitesZoneTemplate</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-allowtrustedsiteszonetemplate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-191">CheckServerCertificateRevocation</span><span class="sxs-lookup"><span data-stu-id="0ad46-191">CheckServerCertificateRevocation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checkservercertificaterevocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-194">CheckSignaturesOnDownloadedPrograms</span><span class="sxs-lookup"><span data-stu-id="0ad46-194">CheckSignaturesOnDownloadedPrograms</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-checksignaturesondownloadedprograms)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-196">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-197">ConsistentMimeHandlingInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-197">ConsistentMimeHandlingInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-consistentmimehandlinginternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-200">DisableAdobeFlash</span><span class="sxs-lookup"><span data-stu-id="0ad46-200">DisableAdobeFlash</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableadobeflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-203">DisableBlockingOfOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-203">DisableBlockingOfOutdatedActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-206">DisableBypassOfSmartScreenWarnings</span><span class="sxs-lookup"><span data-stu-id="0ad46-206">DisableBypassOfSmartScreenWarnings</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarnings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-209">DisableBypassOfSmartScreenWarningsAboutUncommonFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablebypassofsmartscreenwarningsaboutuncommonfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-212">DisableConfiguringHistory</span><span class="sxs-lookup"><span data-stu-id="0ad46-212">DisableConfiguringHistory</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableconfiguringhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-215">DisableCrashDetection</span><span class="sxs-lookup"><span data-stu-id="0ad46-215">DisableCrashDetection</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecrashdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-218">DisableCustomerExperienceImprovementProgramParticipation</span><span class="sxs-lookup"><span data-stu-id="0ad46-218">DisableCustomerExperienceImprovementProgramParticipation</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablecustomerexperienceimprovementprogramparticipation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-221">DisableDeletingUserVisitedWebsites</span><span class="sxs-lookup"><span data-stu-id="0ad46-221">DisableDeletingUserVisitedWebsites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disabledeletinguservisitedwebsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-224">DisableEnclosureDownloading</span><span class="sxs-lookup"><span data-stu-id="0ad46-224">DisableEnclosureDownloading</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableenclosuredownloading)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-227">DisableEncryptionSupport</span><span class="sxs-lookup"><span data-stu-id="0ad46-227">DisableEncryptionSupport</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableencryptionsupport)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-230">DisableFirstRunWizard</span><span class="sxs-lookup"><span data-stu-id="0ad46-230">DisableFirstRunWizard</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablefirstrunwizard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-231">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-233">DisableFlipAheadFeature</span><span class="sxs-lookup"><span data-stu-id="0ad46-233">DisableFlipAheadFeature</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableflipaheadfeature)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-236">DisableHomePageChange</span><span class="sxs-lookup"><span data-stu-id="0ad46-236">DisableHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablehomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-239">DisableIgnoringCertificateErrors</span><span class="sxs-lookup"><span data-stu-id="0ad46-239">DisableIgnoringCertificateErrors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableignoringcertificateerrors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-242">DisableInPrivateBrowsing</span><span class="sxs-lookup"><span data-stu-id="0ad46-242">DisableInPrivateBrowsing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableinprivatebrowsing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-243">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-245">DisableProcessesInEnhancedProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0ad46-245">DisableProcessesInEnhancedProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableprocessesinenhancedprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-248">DisableProxyChange</span><span class="sxs-lookup"><span data-stu-id="0ad46-248">DisableProxyChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disableproxychange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-251">DisableSearchProviderChange</span><span class="sxs-lookup"><span data-stu-id="0ad46-251">DisableSearchProviderChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesearchproviderchange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-254">DisableSecondaryHomePageChange</span><span class="sxs-lookup"><span data-stu-id="0ad46-254">DisableSecondaryHomePageChange</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecondaryhomepagechange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-255">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-257">DisableSecuritySettingsCheck</span><span class="sxs-lookup"><span data-stu-id="0ad46-257">DisableSecuritySettingsCheck</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-disablesecuritysettingscheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-260">DoNotAllowActiveXControlsInProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0ad46-260">DoNotAllowActiveXControlsInProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotallowactivexcontrolsinprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-263">DoNotBlockOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-263">DoNotBlockOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span><span class="sxs-lookup"><span data-stu-id="0ad46-266">DoNotBlockOutdatedActiveXControlsOnSpecificDomains</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-donotblockoutdatedactivexcontrolsonspecificdomains)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-267">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-269">IncludeAllLocalSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-269">IncludeAllLocalSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includealllocalsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-271">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-272">IncludeAllNetworkPaths</span><span class="sxs-lookup"><span data-stu-id="0ad46-272">IncludeAllNetworkPaths</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-includeallnetworkpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-274">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-275">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0ad46-275">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-277">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ad46-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-278">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ad46-278">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-279">InternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-279">InternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-280">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-280">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-281">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-281">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-282">InternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-283">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-284">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-284">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-285">InternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-287">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-287">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-288">InternetZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="0ad46-288">InternetZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-289">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-290">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-290">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-291">InternetZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-293">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-293">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-294">InternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-294">InternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-295">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-295">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-296">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-296">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-297">InternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-297">InternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-298">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-299">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-299">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-300">InternetZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-300">InternetZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-302">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-302">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-303">InternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-303">InternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-305">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-305">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-306">InternetZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-308">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-308">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="0ad46-309">InternetZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-310">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-311">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-311">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-312">InternetZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-313">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-314">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-314">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-315">InternetZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="0ad46-315">InternetZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-316">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-317">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-317">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-318">InternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-318">InternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-319">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-320">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-320">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-321">InternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-321">InternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-322">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-323">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-323">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-324">InternetZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="0ad46-324">InternetZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-326">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-326">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-327">InternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-327">InternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-328">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-329">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-329">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-330">InternetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-332">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-332">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-333">InternetZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-333">InternetZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-334">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-334">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-335">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-335">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-336">InternetZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-336">InternetZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-338">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-338">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-339">InternetZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0ad46-339">InternetZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-340">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-340">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-341">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-341">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="0ad46-342">InternetZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-343">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-344">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-344">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="0ad46-345">InternetZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-346">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-346">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-347">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-347">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-348">InternetZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="0ad46-348">InternetZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-349">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-350">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-350">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-351">InternetZoneEnableProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0ad46-351">InternetZoneEnableProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneenableprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-353">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-353">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="0ad46-354">InternetZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-355">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-356">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-356">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-357">InternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-357">InternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-358">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-358">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-359">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-359">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-360">InternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-360">InternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-361">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-362">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-362">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="0ad46-363">InternetZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-365">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-365">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-366">InternetZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="0ad46-366">InternetZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-367">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-368">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-368">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-369">InternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-369">InternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-370">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-370">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-371">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-371">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0ad46-372">InternetZoneRunNETFrameworkReliantComponentsNotSignedWithAuthenticode</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-373">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-373">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-374">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-374">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0ad46-375">InternetZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-376">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-376">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-377">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-377">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-378">InternetZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-379">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-379">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-380">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-380">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-381">InternetZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="0ad46-381">InternetZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-internetzoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-382">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-383">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-383">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span><span class="sxs-lookup"><span data-stu-id="0ad46-384">InternetZoneWebsitesInLessPrivilegedZonesCanNavigateIntoThisZone</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-385">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-385">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-386">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-386">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-387">IntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-387">IntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-388">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-389">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-389">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-390">IntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-391">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-391">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-392">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-392">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-393">IntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-394">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-394">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-395">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-395">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-396">IntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-396">IntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-397">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-397">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-398">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-398">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-399">IntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-399">IntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-400">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-401">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-401">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-402">IntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-402">IntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-403">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-404">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-404">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-405">IntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-405">IntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-406">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-407">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-407">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-408">IntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-408">IntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-409">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-409">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-410">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-410">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-411">IntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-411">IntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-412">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-413">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-413">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-414">IntranetZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-415">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-415">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-416">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-416">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-417">IntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-417">IntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-418">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-418">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-419">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-419">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="0ad46-420">IntranetZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-421">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-421">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-422">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-422">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-423">IntranetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-423">IntranetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-424">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-425">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-425">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-426">IntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-426">IntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-intranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-427">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-428">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-428">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-429">LocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-429">LocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-430">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-431">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-431">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-432">LocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-433">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-433">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-434">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-434">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-435">LocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-436">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-437">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-437">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-438">LocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-438">LocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-439">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-439">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-440">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-440">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-441">LocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-441">LocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-442">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-443">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-443">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-444">LocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-445">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-446">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-446">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-447">LocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-447">LocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-448">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-448">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-449">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-449">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-450">LocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-450">LocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-451">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-451">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-452">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-452">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-453">LocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-453">LocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-454">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-454">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-455">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-455">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-456">LocalMachineZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-457">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-457">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-458">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-458">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-459">LocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-459">LocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-460">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-460">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-461">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-461">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-462">LocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-462">LocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-463">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-464">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-464">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-465">LocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-465">LocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-localmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-466">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-466">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-467">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-467">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-468">LockedDownInternetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-468">LockedDownInternetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-469">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-470">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-470">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-471">LockedDownInternetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-472">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-472">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-473">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-473">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-474">LockedDownInternetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-475">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-476">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-476">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-477">LockedDownInternetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-477">LockedDownInternetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-478">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-478">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-479">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-479">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-480">LockedDownInternetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-480">LockedDownInternetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-481">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-481">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-482">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-482">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-483">LockedDownInternetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-484">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-484">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-485">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-485">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-486">LockedDownInternetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-486">LockedDownInternetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-487">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-488">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-488">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-489">LockedDownInternetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-489">LockedDownInternetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-490">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-490">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-491">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-491">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-492">LockedDownInternetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-492">LockedDownInternetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-493">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-493">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-494">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-494">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-495">LockedDownInternetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-496">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-496">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-497">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-497">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-498">LockedDownInternetZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-498">LockedDownInternetZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-499">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-499">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-500">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-500">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-501">LockedDownInternetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-501">LockedDownInternetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowninternetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-502">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-502">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-503">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-503">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-504">LockedDownIntranetZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-504">LockedDownIntranetZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-505">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-505">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-506">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-506">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-507">LockedDownIntranetZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-508">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-508">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-509">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-509">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-510">LockedDownIntranetZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-511">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-511">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-512">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-512">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-513">LockedDownIntranetZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-513">LockedDownIntranetZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-514">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-514">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-515">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-515">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-516">LockedDownIntranetZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-517">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-517">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-518">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-518">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-519">LockedDownIntranetZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-520">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-520">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-521">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-521">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-522">LockedDownIntranetZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-522">LockedDownIntranetZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-523">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-523">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-524">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-524">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-525">LockedDownIntranetZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-525">LockedDownIntranetZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-526">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-527">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-527">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-528">LockedDownIntranetZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-528">LockedDownIntranetZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-529">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-530">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-530">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-531">LockedDownIntranetZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-532">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-532">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-533">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-533">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-534">LockedDownIntranetZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownintranetzonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-535">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-536">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-536">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-537">LockedDownLocalMachineZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-538">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-538">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-539">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-539">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-540">LockedDownLocalMachineZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-541">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-541">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-542">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-542">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-543">LockedDownLocalMachineZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-544">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-544">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-545">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-545">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-546">LockedDownLocalMachineZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-546">LockedDownLocalMachineZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-547">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-547">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-548">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-548">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-549">LockedDownLocalMachineZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-550">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-550">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-551">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-551">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-552">LockedDownLocalMachineZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-553">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-553">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-554">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-554">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-555">LockedDownLocalMachineZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-555">LockedDownLocalMachineZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-556">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-556">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-557">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-557">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-558">LockedDownLocalMachineZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-559">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-559">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-560">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-560">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-561">LockedDownLocalMachineZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-562">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-562">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-563">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-563">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-564">LockedDownLocalMachineZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-565">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-565">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-566">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-566">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-567">LockedDownLocalMachineZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-567">LockedDownLocalMachineZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-568">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-568">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-569">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-569">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-570">LockedDownLocalMachineZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownlocalmachinezonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-571">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-572">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-572">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-573">LockedDownRestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-574">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-574">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-575">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-575">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-576">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-577">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-577">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-578">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-578">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-579">LockedDownRestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-580">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-580">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-581">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-581">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-582">LockedDownRestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-583">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-583">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-584">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-584">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-585">LockedDownRestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-586">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-586">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-587">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-587">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-588">LockedDownRestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-589">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-589">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-590">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-590">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-591">LockedDownRestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-591">LockedDownRestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-592">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-592">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-593">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-593">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-594">LockedDownRestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-595">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-595">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-596">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-596">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-597">LockedDownRestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-598">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-599">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-599">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-600">LockedDownRestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-601">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-601">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-602">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-602">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-603">LockedDownRestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-603">LockedDownRestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-604">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-604">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-605">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-605">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-606">LockedDownRestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddownrestrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-607">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-607">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-608">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-608">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-609">LockedDownTrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-610">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-610">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-611">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-611">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-612">LockedDownTrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-613">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-613">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-614">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-614">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-615">LockedDownTrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-616">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-616">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-617">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-617">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-618">LockedDownTrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-618">LockedDownTrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-619">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-619">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-620">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-620">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-621">LockedDownTrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-622">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-622">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-623">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-623">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-624">LockedDownTrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-625">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-625">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-626">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-626">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-627">LockedDownTrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-627">LockedDownTrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-628">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-628">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-629">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-629">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-630">LockedDownTrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-631">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-631">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-632">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-632">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-633">LockedDownTrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-634">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-635">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-635">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-636">LockedDownTrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-637">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-637">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-638">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-638">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-639">LockedDownTrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-639">LockedDownTrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-640">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-641">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-641">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-642">LockedDownTrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-lockeddowntrustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-643">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-643">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-644">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-644">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-645">MimeSniffingSafetyFeatureInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mimesniffingsafetyfeatureinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-646">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-646">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-647">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-647">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-648">MKProtocolSecurityRestrictionInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-mkprotocolsecurityrestrictioninternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-649">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-649">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-650">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-650">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-651">NotificationBarInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-651">NotificationBarInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-notificationbarinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-652">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-652">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-653">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-653">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-654">**ID**</span><span class="sxs-lookup"><span data-stu-id="0ad46-654">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-655">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-655">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-656">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0ad46-656">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-657">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ad46-657">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-658">PreventManagingSmartScreenFilter</span><span class="sxs-lookup"><span data-stu-id="0ad46-658">PreventManagingSmartScreenFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventmanagingsmartscreenfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-659">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-659">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-660">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-660">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-661">PreventPerUserInstallationOfActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-661">PreventPerUserInstallationOfActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-preventperuserinstallationofactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-662">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-663">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-663">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-664">ProtectionFromZoneElevationInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-664">ProtectionFromZoneElevationInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-protectionfromzoneelevationinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-665">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-665">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-666">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-666">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-667">RemoveRunThisTimeButtonForOutdatedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-removerunthistimebuttonforoutdatedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-668">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-668">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-669">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-669">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-670">RestrictActiveXInstallInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-670">RestrictActiveXInstallInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictactivexinstallinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-671">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-671">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-672">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-672">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-673">RestrictedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-673">RestrictedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-674">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-674">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-675">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-675">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-676">RestrictedSitesZoneAllowActiveScripting</span><span class="sxs-lookup"><span data-stu-id="0ad46-676">RestrictedSitesZoneAllowActiveScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowactivescripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-677">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-677">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-678">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-678">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-679">RestrictedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-680">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-680">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-681">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-681">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-682">RestrictedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-683">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-683">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-684">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-684">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span><span class="sxs-lookup"><span data-stu-id="0ad46-685">RestrictedSitesZoneAllowBinaryAndScriptBehaviors</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowbinaryandscriptbehaviors)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-686">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-687">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-687">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-688">RestrictedSitesZoneAllowCopyPasteViaScript</span><span class="sxs-lookup"><span data-stu-id="0ad46-688">RestrictedSitesZoneAllowCopyPasteViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowcopypasteviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-689">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-689">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-690">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-690">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-691">RestrictedSitesZoneAllowDragAndDropCopyAndPasteFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowdraganddropcopyandpastefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-692">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-692">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-693">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-693">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-694">RestrictedSitesZoneAllowFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-694">RestrictedSitesZoneAllowFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-695">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-695">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-696">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-696">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-697">RestrictedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-697">RestrictedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-698">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-698">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-699">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-699">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-700">RestrictedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-700">RestrictedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-701">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-701">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-702">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-702">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-703">RestrictedSitesZoneAllowLoadingOfXAMLFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowloadingofxamlfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-704">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-704">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-705">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-705">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-706">RestrictedSitesZoneAllowMETAREFRESH</span><span class="sxs-lookup"><span data-stu-id="0ad46-706">RestrictedSitesZoneAllowMETAREFRESH</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowmetarefresh)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-707">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-707">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-708">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-708">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-709">RestrictedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-710">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-710">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-711">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-711">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-712">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstouseactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-713">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-713">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-714">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-714">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span><span class="sxs-lookup"><span data-stu-id="0ad46-715">RestrictedSitesZoneAllowOnlyApprovedDomainsToUseTDCActiveXControl</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowonlyapproveddomainstousetdcactivexcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-716">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-716">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-717">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-717">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-718">RestrictedSitesZoneAllowScriptingOfInternetExplorerWebBrowserControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptingofinternetexplorerwebbrowsercontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-719">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-719">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-720">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-720">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span><span class="sxs-lookup"><span data-stu-id="0ad46-721">RestrictedSitesZoneAllowScriptInitiatedWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptinitiatedwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-722">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-722">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-723">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-723">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-724">RestrictedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-724">RestrictedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-725">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-725">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-726">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-726">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-727">RestrictedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-727">RestrictedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-728">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-728">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-729">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-729">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span><span class="sxs-lookup"><span data-stu-id="0ad46-730">RestrictedSitesZoneAllowUpdatesToStatusBarViaScript</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowupdatestostatusbarviascript)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-731">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-731">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-732">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-732">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-733">RestrictedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-733">RestrictedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-734">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-734">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-735">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-735">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-736">RestrictedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-737">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-737">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-738">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-738">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-739">RestrictedSitesZoneDownloadSignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-739">RestrictedSitesZoneDownloadSignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-740">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-740">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-741">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-741">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-742">RestrictedSitesZoneDownloadUnsignedActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonedownloadunsignedactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-743">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-743">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-744">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-744">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0ad46-745">RestrictedSitesZoneEnableCrossSiteScriptingFilter</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablecrosssitescriptingfilter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-746">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-746">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-747">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-747">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span><span class="sxs-lookup"><span data-stu-id="0ad46-748">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsAcrossWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainsacrosswindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-749">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-749">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-750">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-750">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span><span class="sxs-lookup"><span data-stu-id="0ad46-751">RestrictedSitesZoneEnableDraggingOfContentFromDifferentDomainsWithinWindows</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenabledraggingofcontentfromdifferentdomainswithinwindows)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-752">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-752">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-753">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-753">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-754">RestrictedSitesZoneEnableMIMESniffing</span><span class="sxs-lookup"><span data-stu-id="0ad46-754">RestrictedSitesZoneEnableMIMESniffing</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneenablemimesniffing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-755">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-755">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-756">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-756">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span><span class="sxs-lookup"><span data-stu-id="0ad46-757">RestrictedSitesZoneIncludeLocalPathWhenUploadingFilesToServer</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneincludelocalpathwhenuploadingfilestoserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-758">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-758">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-759">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-759">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-760">RestrictedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-761">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-761">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-762">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-762">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-763">RestrictedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-763">RestrictedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-764">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-764">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-765">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-765">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span><span class="sxs-lookup"><span data-stu-id="0ad46-766">RestrictedSitesZoneLaunchingApplicationsAndFilesInIFRAME</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelaunchingapplicationsandfilesiniframe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-767">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-767">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-768">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-768">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-769">RestrictedSitesZoneLogonOptions</span><span class="sxs-lookup"><span data-stu-id="0ad46-769">RestrictedSitesZoneLogonOptions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonelogonoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-770">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-770">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-771">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-771">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-772">RestrictedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-772">RestrictedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-773">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-773">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-774">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-774">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span><span class="sxs-lookup"><span data-stu-id="0ad46-775">RestrictedSitesZoneNavigateWindowsAndFramesAcrossDomains</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-776">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-776">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-777">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-777">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span><span class="sxs-lookup"><span data-stu-id="0ad46-778">RestrictedSitesZoneRunActiveXControlsAndPlugins</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunactivexcontrolsandplugins)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-779">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-779">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-780">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-780">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span><span class="sxs-lookup"><span data-stu-id="0ad46-781">RestrictedSitesZoneRunNETFrameworkReliantComponentsSignedWithAuthenticode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonerunnetframeworkreliantcomponentssignedwithauthenticode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-782">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-782">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-783">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-783">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span><span class="sxs-lookup"><span data-stu-id="0ad46-784">RestrictedSitesZoneScriptActiveXControlsMarkedSafeForScripting</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptactivexcontrolsmarkedsafeforscripting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-785">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-785">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-786">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-786">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-787">RestrictedSitesZoneScriptingOfJavaApplets</span><span class="sxs-lookup"><span data-stu-id="0ad46-787">RestrictedSitesZoneScriptingOfJavaApplets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszonescriptingofjavaapplets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-788">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-788">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-789">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-789">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span><span class="sxs-lookup"><span data-stu-id="0ad46-790">RestrictedSitesZoneShowSecurityWarningForPotentiallyUnsafeFiles</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneshowsecuritywarningforpotentiallyunsafefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-791">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-791">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-792">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-792">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span><span class="sxs-lookup"><span data-stu-id="0ad46-793">RestrictedSitesZoneTurnOnCrossSiteScriptingFilter</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-794">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-794">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-795">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-795">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-796">RestrictedSitesZoneTurnOnProtectedMode</span><span class="sxs-lookup"><span data-stu-id="0ad46-796">RestrictedSitesZoneTurnOnProtectedMode</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneturnonprotectedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-797">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-797">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-798">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-798">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-799">RestrictedSitesZoneUsePopupBlocker</span><span class="sxs-lookup"><span data-stu-id="0ad46-799">RestrictedSitesZoneUsePopupBlocker</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictedsiteszoneusepopupblocker)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-800">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-800">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-801">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-801">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-802">RestrictFileDownloadInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-802">RestrictFileDownloadInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-restrictfiledownloadinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-803">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-803">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-804">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-804">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span><span class="sxs-lookup"><span data-stu-id="0ad46-805">ScriptedWindowSecurityRestrictionsInternetExplorerProcesses</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-scriptedwindowsecurityrestrictionsinternetexplorerprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-806">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-806">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-807">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-807">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-808">SearchProviderList</span><span class="sxs-lookup"><span data-stu-id="0ad46-808">SearchProviderList</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-searchproviderlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-809">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-809">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-810">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-810">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-811">SpecifyUseOfActiveXInstallerService</span><span class="sxs-lookup"><span data-stu-id="0ad46-811">SpecifyUseOfActiveXInstallerService</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-specifyuseofactivexinstallerservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-812">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-812">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-813">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-813">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-814">TrustedSitesZoneAllowAccessToDataSources</span><span class="sxs-lookup"><span data-stu-id="0ad46-814">TrustedSitesZoneAllowAccessToDataSources</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowaccesstodatasources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-815">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-815">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-816">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-816">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-817">TrustedSitesZoneAllowAutomaticPromptingForActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-818">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-818">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-819">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-819">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-820">TrustedSitesZoneAllowAutomaticPromptingForFileDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowautomaticpromptingforfiledownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-821">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-821">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-822">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-822">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-823">TrustedSitesZoneAllowFontDownloads</span><span class="sxs-lookup"><span data-stu-id="0ad46-823">TrustedSitesZoneAllowFontDownloads</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowfontdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-824">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-824">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-825">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-825">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-826">TrustedSitesZoneAllowLessPrivilegedSites</span><span class="sxs-lookup"><span data-stu-id="0ad46-826">TrustedSitesZoneAllowLessPrivilegedSites</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowlessprivilegedsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-827">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-827">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-828">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-828">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span><span class="sxs-lookup"><span data-stu-id="0ad46-829">TrustedSitesZoneAllowNETFrameworkReliantComponents</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallownetframeworkreliantcomponents)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-830">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-830">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-831">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-831">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-832">TrustedSitesZoneAllowScriptlets</span><span class="sxs-lookup"><span data-stu-id="0ad46-832">TrustedSitesZoneAllowScriptlets</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowscriptlets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-833">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-833">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-834">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-834">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-835">TrustedSitesZoneAllowSmartScreenIE</span><span class="sxs-lookup"><span data-stu-id="0ad46-835">TrustedSitesZoneAllowSmartScreenIE</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowsmartscreenie)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-836">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-836">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-837">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-837">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-838">TrustedSitesZoneAllowUserDataPersistence</span><span class="sxs-lookup"><span data-stu-id="0ad46-838">TrustedSitesZoneAllowUserDataPersistence</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneallowuserdatapersistence)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-839">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-839">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-840">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-840">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-841">TrustedSitesZoneDoNotRunAntimalwareAgainstActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonedonotrunantimalwareagainstactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-842">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-842">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-843">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-843">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-844">TrustedSitesZoneDontRunAntimalwareProgramsAgainstActiveXControls</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-845">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-845">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-846">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-846">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span><span class="sxs-lookup"><span data-stu-id="0ad46-847">TrustedSitesZoneInitializeAndScriptActiveXControls</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszoneinitializeandscriptactivexcontrols)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-848">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-848">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-849">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-849">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span><span class="sxs-lookup"><span data-stu-id="0ad46-850">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedAsSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-851">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-851">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-852">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-852">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0ad46-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span><span class="sxs-lookup"><span data-stu-id="0ad46-853">TrustedSitesZoneInitializeAndScriptActiveXControlsNotMarkedSafe</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-854">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-854">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-855">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-855">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-856">TrustedSitesZoneJavaPermissions</span><span class="sxs-lookup"><span data-stu-id="0ad46-856">TrustedSitesZoneJavaPermissions</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonejavapermissions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-857">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-857">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-858">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-858">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0ad46-859">TrustedSitesZoneNavigateWindowsAndFrames</span><span class="sxs-lookup"><span data-stu-id="0ad46-859">TrustedSitesZoneNavigateWindowsAndFrames</span></span>](/windows/client-management/mdm/policy-csp-internetexplorer#internetexplorer-trustedsiteszonenavigatewindowsandframes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ad46-860">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0ad46-860">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ad46-861">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0ad46-861">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ad46-862">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ad46-862">Requirements</span></span>



| <span data-ttu-id="0ad46-863">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ad46-863">Requirement</span></span> | <span data-ttu-id="0ad46-864">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ad46-864">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ad46-865">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ad46-865">Minimum supported client</span></span><br/> | <span data-ttu-id="0ad46-866">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ad46-866">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ad46-867">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ad46-867">Minimum supported server</span></span><br/> | <span data-ttu-id="0ad46-868">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ad46-868">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0ad46-869">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0ad46-869">Namespace</span></span><br/>                | <span data-ttu-id="0ad46-870">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="0ad46-870">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0ad46-871">MOF</span><span class="sxs-lookup"><span data-stu-id="0ad46-871">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ad46-872"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ad46-872"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ad46-873">DLL</span><span class="sxs-lookup"><span data-stu-id="0ad46-873">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ad46-874"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ad46-874"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

