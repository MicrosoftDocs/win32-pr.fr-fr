---
title: Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02
description: La \_ classe Result01 LocalPoliciesSecurityOptions02 de la stratégie MDM \_ \_ représente les options de sécurité stratégies locales.
ms.assetid: 75ac4789-781f-4722-8b0a-33e53b307296
keywords:
- Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- Classe MDM_Policy_Result01_LocalPoliciesSecurityOptions02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.InstanceID
- MDM_Policy_Result01_LocalPoliciesSecurityOptions02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f1ece3790bf5a6a6ac51310d04661366bbe9e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032744"
---
# <a name="mdm_policy_result01_localpoliciessecurityoptions02-class"></a><span data-ttu-id="52317-105">\_Classe LocalPoliciesSecurityOptions02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="52317-105">MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class</span></span>

<span data-ttu-id="52317-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="52317-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="52317-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="52317-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="52317-108">La \_ classe Result01 LocalPoliciesSecurityOptions02 de la stratégie MDM \_ \_ représente les options de sécurité stratégies locales.</span><span class="sxs-lookup"><span data-stu-id="52317-108">The MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02 class represents the local policies security options.</span></span>

<span data-ttu-id="52317-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="52317-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52317-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52317-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LocalPoliciesSecurityOptions02
{
  string InstanceID;
  string ParentID;
  sint32 Accounts_BlockMicrosoftAccounts;
  sint32 Accounts_EnableGuestAccountStatus;
  sint32 Accounts_EnableAdministratorAccountStatus;
  sint32 Accounts_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly;
  string Accounts_RenameAdministratorAccount;
  string Accounts_RenameGuestAccount;
  string Devices_RestrictCDROMAccessToLocallyLoggedOnUserOnly;
  sint32 Devices_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters;
  sint32 Devices_AllowUndockWithoutHavingToLogon;
  string Devices_AllowedToFormatAndEjectRemovableMedia;
  sint32 InteractiveLogon_DisplayUserInformationWhenTheSessionIsLocked;
  sint32 Interactivelogon_DoNotDisplayLastSignedIn;
  sint32 Interactivelogon_DoNotDisplayUsernameAtSignIn;
  sint32 Interactivelogon_DoNotRequireCTRLALTDEL;
  sint32 InteractiveLogon_MachineInactivityLimit;
  string InteractiveLogon_MessageTextForUsersAttemptingToLogOn;
  string InteractiveLogon_MessageTitleForUsersAttemptingToLogOn;
  sint32 NetworkAccess_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares;
  sint32 NetworkAccess_RestrictAnonymousAccessToNamedPipesAndShares;
  string NetworkAccess_RestrictClientsAllowedToMakeRemoteCallsToSAM;
  sint32 NetworkSecurity_AllowPKU2UAuthenticationRequests;
  sint32 RecoveryConsole_AllowAutomaticAdministrativeLogon;
  sint32 Shutdown_AllowSystemToBeShutDownWithoutHavingToLogOn;
  sint32 Shutdown_ClearVirtualMemoryPageFile;
  sint32 UserAccountControl_AllowUIAccessApplicationsToPromptForElevation;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForAdministrators;
  sint32 UserAccountControl_BehaviorOfTheElevationPromptForStandardUsers;
  sint32 UserAccountControl_DetectApplicationInstallationsAndPromptForElevation;
  sint32 UserAccountControl_OnlyElevateExecutableFilesThatAreSignedAndValidated;
  sint32 UserAccountControl_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations;
  sint32 UserAccountControl_RunAllAdministratorsInAdminApprovalMode;
  sint32 UserAccountControl_SwitchToTheSecureDesktopWhenPromptingForElevation;
  sint32 UserAccountControl_UseAdminApprovalMode;
  sint32 UserAccountControl_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations;
};
```

## <a name="members"></a><span data-ttu-id="52317-111">Membres</span><span class="sxs-lookup"><span data-stu-id="52317-111">Members</span></span>

<span data-ttu-id="52317-112">La **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52317-112">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these types of members:</span></span>

-   [<span data-ttu-id="52317-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52317-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52317-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52317-114">Properties</span></span>

<span data-ttu-id="52317-115">La **classe \_ \_ Result01 \_ LocalPoliciesSecurityOptions02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="52317-115">The **MDM\_Policy\_Result01\_LocalPoliciesSecurityOptions02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="52317-116">Comptes \_ BlockMicrosoftAccounts</span><span class="sxs-lookup"><span data-stu-id="52317-116">Accounts\_BlockMicrosoftAccounts</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-blockmicrosoftaccounts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52317-119">Accounts_EnableAdministratorAccountStatus</span><span class="sxs-lookup"><span data-stu-id="52317-119">Accounts_EnableAdministratorAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52317-122">Accounts_EnableGuestAccountStatus</span><span class="sxs-lookup"><span data-stu-id="52317-122">Accounts_EnableGuestAccountStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-125">Comptes \_ LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span><span class="sxs-lookup"><span data-stu-id="52317-125">Accounts\_LimitLocalAccountUseOfBlankPasswordsToConsoleLogonOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-limitlocalaccountuseofblankpasswordstoconsolelogononly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-128">Comptes \_ RenameAdministratorAccount</span><span class="sxs-lookup"><span data-stu-id="52317-128">Accounts\_RenameAdministratorAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameadministratoraccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-131">Comptes \_ RenameGuestAccount</span><span class="sxs-lookup"><span data-stu-id="52317-131">Accounts\_RenameGuestAccount</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-accounts-renameguestaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-132">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-134">Appareils \_ AllowedToFormatAndEjectRemovableMedia</span><span class="sxs-lookup"><span data-stu-id="52317-134">Devices\_AllowedToFormatAndEjectRemovableMedia</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowedtoformatandejectremovablemedia)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-137">Appareils \_ AllowUndockWithoutHavingToLogon</span><span class="sxs-lookup"><span data-stu-id="52317-137">Devices\_AllowUndockWithoutHavingToLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-allowundockwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-140">Appareils \_ PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span><span class="sxs-lookup"><span data-stu-id="52317-140">Devices\_PreventUsersFromInstallingPrinterDriversWhenConnectingToSharedPrinters</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-preventusersfrominstallingprinterdriverswhenconnectingtosharedprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-143">Appareils \_ RestrictCDROMAccessToLocallyLoggedOnUserOnly</span><span class="sxs-lookup"><span data-stu-id="52317-143">Devices\_RestrictCDROMAccessToLocallyLoggedOnUserOnly</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-devices-restrictcdromaccesstolocallyloggedonuseronly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52317-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="52317-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52317-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52317-149">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52317-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-150">InteractiveLogon \_ DisplayUserInformationWhenTheSessionIsLocked</span><span class="sxs-lookup"><span data-stu-id="52317-150">InteractiveLogon\_DisplayUserInformationWhenTheSessionIsLocked</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-displayuserinformationwhenthesessionislocked)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-151">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-151">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-153">Interactivelogon \_ DoNotDisplayLastSignedIn</span><span class="sxs-lookup"><span data-stu-id="52317-153">Interactivelogon\_DoNotDisplayLastSignedIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplaylastsignedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-154">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-155">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-156">Interactivelogon \_ DoNotDisplayUsernameAtSignIn</span><span class="sxs-lookup"><span data-stu-id="52317-156">Interactivelogon\_DoNotDisplayUsernameAtSignIn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotdisplayusernameatsignin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-157">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-158">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-159">Interactivelogon \_ DoNotRequireCTRLALTDEL</span><span class="sxs-lookup"><span data-stu-id="52317-159">Interactivelogon\_DoNotRequireCTRLALTDEL</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-donotrequirectrlaltdel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-160">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-161">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-162">InteractiveLogon \_ MachineInactivityLimit</span><span class="sxs-lookup"><span data-stu-id="52317-162">InteractiveLogon\_MachineInactivityLimit</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-machineinactivitylimit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-163">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-164">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-165">InteractiveLogon \_ MessageTextForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="52317-165">InteractiveLogon\_MessageTextForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetextforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-168">InteractiveLogon \_ MessageTitleForUsersAttemptingToLogOn</span><span class="sxs-lookup"><span data-stu-id="52317-168">InteractiveLogon\_MessageTitleForUsersAttemptingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-interactivelogon-messagetitleforusersattemptingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-170">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-171">NetworkAccess \_ DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span><span class="sxs-lookup"><span data-stu-id="52317-171">NetworkAccess\_DoNotAllowAnonymousEnumerationOfSAMAccountsAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-donotallowanonymousenumerationofsamaccountsandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-172">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-172">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-174">NetworkAccess \_ RestrictAnonymousAccessToNamedPipesAndShares</span><span class="sxs-lookup"><span data-stu-id="52317-174">NetworkAccess\_RestrictAnonymousAccessToNamedPipesAndShares</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictanonymousaccesstonamedpipesandshares)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-175">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-175">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-176">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-176">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-177">NetworkAccess \_ RestrictClientsAllowedToMakeRemoteCallsToSAM</span><span class="sxs-lookup"><span data-stu-id="52317-177">NetworkAccess\_RestrictClientsAllowedToMakeRemoteCallsToSAM</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networkaccess-restrictclientsallowedtomakeremotecallstosam)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-179">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-179">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-180">NetworkSecurity \_ AllowPKU2UAuthenticationRequests</span><span class="sxs-lookup"><span data-stu-id="52317-180">NetworkSecurity\_AllowPKU2UAuthenticationRequests</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-networksecurity-allowpku2uauthenticationrequests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-181">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-182">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="52317-183">**ID**</span><span class="sxs-lookup"><span data-stu-id="52317-183">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-184">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52317-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52317-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52317-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52317-186">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52317-186">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-187">RecoveryConsole \_ AllowAutomaticAdministrativeLogon</span><span class="sxs-lookup"><span data-stu-id="52317-187">RecoveryConsole\_AllowAutomaticAdministrativeLogon</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-recoveryconsole-allowautomaticadministrativelogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-188">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-188">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-189">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-190">Arrêter \_ AllowSystemToBeShutDownWithoutHavingToLogOn</span><span class="sxs-lookup"><span data-stu-id="52317-190">Shutdown\_AllowSystemToBeShutDownWithoutHavingToLogOn</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-allowsystemtobeshutdownwithouthavingtologon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-191">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-191">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-192">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-193">Arrêter \_ ClearVirtualMemoryPageFile</span><span class="sxs-lookup"><span data-stu-id="52317-193">Shutdown\_ClearVirtualMemoryPageFile</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-shutdown-clearvirtualmemorypagefile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-194">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-194">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-195">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-196">UserAccountControl \_ AllowUIAccessApplicationsToPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="52317-196">UserAccountControl\_AllowUIAccessApplicationsToPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-allowuiaccessapplicationstopromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-197">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-197">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-198">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-199">UserAccountControl \_ BehaviorOfTheElevationPromptForAdministrators</span><span class="sxs-lookup"><span data-stu-id="52317-199">UserAccountControl\_BehaviorOfTheElevationPromptForAdministrators</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-200">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-201">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-202">UserAccountControl \_ BehaviorOfTheElevationPromptForStandardUsers</span><span class="sxs-lookup"><span data-stu-id="52317-202">UserAccountControl\_BehaviorOfTheElevationPromptForStandardUsers</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-behavioroftheelevationpromptforstandardusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-203">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-203">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-204">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-205">UserAccountControl \_ DetectApplicationInstallationsAndPromptForElevation</span><span class="sxs-lookup"><span data-stu-id="52317-205">UserAccountControl\_DetectApplicationInstallationsAndPromptForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-detectapplicationinstallationsandpromptforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-206">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-206">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-207">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-208">UserAccountControl \_ OnlyElevateExecutableFilesThatAreSignedAndValidated</span><span class="sxs-lookup"><span data-stu-id="52317-208">UserAccountControl\_OnlyElevateExecutableFilesThatAreSignedAndValidated</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateexecutablefilesthataresignedandvalidated)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-209">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-210">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-210">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-211">UserAccountControl \_ OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span><span class="sxs-lookup"><span data-stu-id="52317-211">UserAccountControl\_OnlyElevateUIAccessApplicationsThatAreInstalledInSecureLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-onlyelevateuiaccessapplicationsthatareinstalledinsecurelocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-212">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-212">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-213">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-213">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-214">UserAccountControl \_ RunAllAdministratorsInAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="52317-214">UserAccountControl\_RunAllAdministratorsInAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-runalladministratorsinadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-215">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-216">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-216">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-217">UserAccountControl \_ SwitchToTheSecureDesktopWhenPromptingForElevation</span><span class="sxs-lookup"><span data-stu-id="52317-217">UserAccountControl\_SwitchToTheSecureDesktopWhenPromptingForElevation</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-switchtothesecuredesktopwhenpromptingforelevation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-218">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-218">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-219">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-219">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-220">UserAccountControl \_ UseAdminApprovalMode</span><span class="sxs-lookup"><span data-stu-id="52317-220">UserAccountControl\_UseAdminApprovalMode</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-useadminapprovalmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-221">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-221">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-222">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-222">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52317-223">UserAccountControl \_ VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span><span class="sxs-lookup"><span data-stu-id="52317-223">UserAccountControl\_VirtualizeFileAndRegistryWriteFailuresToPerUserLocations</span></span>](/windows/client-management/mdm/policy-csp-localpoliciessecurityoptions#localpoliciessecurityoptions-useraccountcontrol-virtualizefileandregistrywritefailurestoperuserlocations)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52317-224">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="52317-224">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="52317-225">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52317-225">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52317-226">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52317-226">Requirements</span></span>



| <span data-ttu-id="52317-227">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52317-227">Requirement</span></span> | <span data-ttu-id="52317-228">Valeur</span><span class="sxs-lookup"><span data-stu-id="52317-228">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52317-229">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52317-229">Minimum supported client</span></span><br/> | <span data-ttu-id="52317-230">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52317-230">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52317-231">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52317-231">Minimum supported server</span></span><br/> | <span data-ttu-id="52317-232">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="52317-232">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="52317-233">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52317-233">Namespace</span></span><br/>                | <span data-ttu-id="52317-234">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="52317-234">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="52317-235">MOF</span><span class="sxs-lookup"><span data-stu-id="52317-235">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52317-236"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52317-236"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="52317-237">DLL</span><span class="sxs-lookup"><span data-stu-id="52317-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52317-238"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52317-238"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

