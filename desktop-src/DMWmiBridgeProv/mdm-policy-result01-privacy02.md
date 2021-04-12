---
title: MDM_Policy_Result01_Privacy02, classe
description: La \_ classe Privacy02 de la stratégie MDM \_ Result01 \_ représente les stratégies de recherche disponibles.
ms.assetid: 40aa1b74-bdec-471d-a7d4-89e59bf8637c
keywords:
- MDM_Policy_Result01_Privacy02, classe
- Classe MDM_Policy_Result01_Privacy02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Privacy02
- MDM_Policy_Result01_Privacy02.InstanceID
- MDM_Policy_Result01_Privacy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bbe28d1c0bc1258ec3c9fb57fd592a97c96026
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464379"
---
# <a name="mdm_policy_result01_privacy02-class"></a><span data-ttu-id="8ca71-105">\_Classe Privacy02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="8ca71-105">MDM\_Policy\_Result01\_Privacy02 class</span></span>

<span data-ttu-id="8ca71-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="8ca71-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8ca71-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="8ca71-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8ca71-108">La classe Privacy02 de la **\_ stratégie MDM \_ Result01 \_** représente les stratégies de recherche disponibles.</span><span class="sxs-lookup"><span data-stu-id="8ca71-108">The **MDM\_Policy\_Result01\_Privacy02** class represents the search policies available.</span></span>

<span data-ttu-id="8ca71-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="8ca71-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca71-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ca71-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Privacy02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAutoAcceptPairingAndPrivacyConsentPrompts;
  sint32 AllowInputPersonalization;
  string LetAppsSyncWithDevices_UserInControlOfTheseApps;
  sint32 PublishUserActivities;
  string LetAppsSyncWithDevices_ForceDenyTheseApps;
  string LetAppsSyncWithDevices_ForceAllowTheseApps;
  sint32 LetAppsSyncWithDevices;
  string LetAppsAccessTrustedDevices_UserInControlOfTheseApps;
  string LetAppsRunInBackground_UserInControlOfTheseApps;
  string LetAppsRunInBackground_ForceDenyTheseApps;
  string LetAppsRunInBackground_ForceAllowTheseApps;
  sint32 LetAppsRunInBackground;
  string LetAppsGetDiagnosticInfo_UserInControlOfTheseApps;
  string LetAppsGetDiagnosticInfo_ForceDenyTheseApps;
  string LetAppsGetDiagnosticInfo_ForceAllowTheseApps;
  sint32 LetAppsGetDiagnosticInfo;
  string LetAppsAccessTrustedDevices_ForceDenyTheseApps;
  string LetAppsAccessTrustedDevices_ForceAllowTheseApps;
  sint32 LetAppsAccessTrustedDevices;
  string LetAppsAccessRadios_UserInControlOfTheseApps;
  string LetAppsAccessTasks_UserInControlOfTheseApps;
  string LetAppsAccessTasks_ForceDenyTheseApps;
  string LetAppsAccessTasks_ForceAllowTheseApps;
  sint32 LetAppsAccessTasks;
  string LetAppsAccessRadios_ForceDenyTheseApps;
  string LetAppsAccessRadios_ForceAllowTheseApps;
  sint32 LetAppsAccessRadios;
  string LetAppsAccessPhone_UserInControlOfTheseApps;
  string LetAppsAccessPhone_ForceDenyTheseApps;
  string LetAppsAccessPhone_ForceAllowTheseApps;
  sint32 LetAppsAccessPhone;
  string LetAppsAccessMotion_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_UserInControlOfTheseApps;
  string LetAppsAccessNotifications_ForceDenyTheseApps;
  string LetAppsAccessNotifications_ForceAllowTheseApps;
  sint32 LetAppsAccessNotifications;
  string LetAppsAccessMotion_ForceDenyTheseApps;
  string LetAppsAccessMotion_ForceAllowTheseApps;
  sint32 LetAppsAccessMotion;
  string LetAppsAccessMicrophone_UserInControlOfTheseApps;
  string LetAppsAccessMicrophone_ForceDenyTheseApps;
  string LetAppsAccessMicrophone_ForceAllowTheseApps;
  sint32 LetAppsAccessMicrophone;
  string LetAppsAccessMessaging_UserInControlOfTheseApps;
  string LetAppsAccessMessaging_ForceDenyTheseApps;
  string LetAppsAccessMessaging_ForceAllowTheseApps;
  sint32 LetAppsAccessMessaging;
  string LetAppsAccessLocation_UserInControlOfTheseApps;
  string LetAppsAccessLocation_ForceDenyTheseApps;
  string LetAppsAccessLocation_ForceAllowTheseApps;
  sint32 LetAppsAccessLocation;
  string LetAppsAccessEmail_UserInControlOfTheseApps;
  string LetAppsAccessEmail_ForceDenyTheseApps;
  string LetAppsAccessEmail_ForceAllowTheseApps;
  sint32 LetAppsAccessEmail;
  string LetAppsAccessContacts_UserInControlOfTheseApps;
  string LetAppsAccessContacts_ForceDenyTheseApps;
  string LetAppsAccessContacts_ForceAllowTheseApps;
  sint32 LetAppsAccessContacts;
  string LetAppsAccessCamera_UserInControlOfTheseApps;
  string LetAppsAccessCamera_ForceDenyTheseApps;
  string LetAppsAccessCamera_ForceAllowTheseApps;
  sint32 LetAppsAccessCamera;
  string LetAppsAccessCallHistory_UserInControlOfTheseApps;
  string LetAppsAccessCallHistory_ForceDenyTheseApps;
  string LetAppsAccessCallHistory_ForceAllowTheseApps;
  sint32 LetAppsAccessCallHistory;
  string LetAppsAccessCalendar_UserInControlOfTheseApps;
  string LetAppsAccessCalendar_ForceDenyTheseApps;
  string LetAppsAccessCalendar_ForceAllowTheseApps;
  sint32 LetAppsAccessCalendar;
  string LetAppsAccessAccountInfo_UserInControlOfTheseApps;
  string LetAppsAccessAccountInfo_ForceDenyTheseApps;
  string LetAppsAccessAccountInfo_ForceAllowTheseApps;
  sint32 LetAppsAccessAccountInfo;
  sint32 DisableAdvertisingId;
  sint32 EnableActivityFeed;
};
```

## <a name="members"></a><span data-ttu-id="8ca71-111">Membres</span><span class="sxs-lookup"><span data-stu-id="8ca71-111">Members</span></span>

<span data-ttu-id="8ca71-112">La **classe \_ \_ Result01 \_ Privacy02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8ca71-112">The **MDM\_Policy\_Result01\_Privacy02** class has these types of members:</span></span>

-   [<span data-ttu-id="8ca71-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ca71-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ca71-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8ca71-114">Properties</span></span>

<span data-ttu-id="8ca71-115">La **classe \_ \_ Result01 \_ Privacy02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8ca71-115">The **MDM\_Policy\_Result01\_Privacy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8ca71-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span><span class="sxs-lookup"><span data-stu-id="8ca71-116">AllowAutoAcceptPairingAndPrivacyConsentPrompts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowautoacceptpairingandprivacyconsentprompts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-119">AllowInputPersonalization</span><span class="sxs-lookup"><span data-stu-id="8ca71-119">AllowInputPersonalization</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-allowinputpersonalization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-122">DisableAdvertisingId</span><span class="sxs-lookup"><span data-stu-id="8ca71-122">DisableAdvertisingId</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-disableadvertisingid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-125">EnableActivityFeed</span><span class="sxs-lookup"><span data-stu-id="8ca71-125">EnableActivityFeed</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-enableactivityfeed)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ca71-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ca71-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ca71-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ca71-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8ca71-132">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8ca71-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="8ca71-133">Pour cette classe, la chaîne est « privacy ».</span><span class="sxs-lookup"><span data-stu-id="8ca71-133">For this class, the string is "Privacy".</span></span>

</dd> <dt>

[<span data-ttu-id="8ca71-134">LetAppsAccessAccountInfo</span><span class="sxs-lookup"><span data-stu-id="8ca71-134">LetAppsAccessAccountInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-137">LetAppsAccessAccountInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-137">LetAppsAccessAccountInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-140">LetAppsAccessAccountInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-140">LetAppsAccessAccountInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-143">LetAppsAccessAccountInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-143">LetAppsAccessAccountInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessaccountinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-146">LetAppsAccessCalendar</span><span class="sxs-lookup"><span data-stu-id="8ca71-146">LetAppsAccessCalendar</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-149">LetAppsAccessCalendar \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-149">LetAppsAccessCalendar\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-150">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-152">LetAppsAccessCalendar \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-152">LetAppsAccessCalendar\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-155">LetAppsAccessCalendar \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-155">LetAppsAccessCalendar\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscalendar-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-157">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-158">LetAppsAccessCallHistory</span><span class="sxs-lookup"><span data-stu-id="8ca71-158">LetAppsAccessCallHistory</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-159">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-160">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-161">LetAppsAccessCallHistory \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-161">LetAppsAccessCallHistory\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-164">LetAppsAccessCallHistory \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-164">LetAppsAccessCallHistory\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-165">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-166">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-167">LetAppsAccessCallHistory \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-167">LetAppsAccessCallHistory\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscallhistory-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-170">LetAppsAccessCamera</span><span class="sxs-lookup"><span data-stu-id="8ca71-170">LetAppsAccessCamera</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-171">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-172">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-173">LetAppsAccessCamera \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-173">LetAppsAccessCamera\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-174">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-175">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-176">LetAppsAccessCamera \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-176">LetAppsAccessCamera\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-179">LetAppsAccessCamera \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-179">LetAppsAccessCamera\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscamera-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-182">LetAppsAccessContacts</span><span class="sxs-lookup"><span data-stu-id="8ca71-182">LetAppsAccessContacts</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-183">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-185">LetAppsAccessContacts \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-185">LetAppsAccessContacts\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-186">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-187">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-188">LetAppsAccessContacts \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-188">LetAppsAccessContacts\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-189">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-190">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-191">LetAppsAccessContacts \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-191">LetAppsAccessContacts\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesscontacts-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-193">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-194">LetAppsAccessEmail</span><span class="sxs-lookup"><span data-stu-id="8ca71-194">LetAppsAccessEmail</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-195">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-195">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-196">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-196">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-197">LetAppsAccessEmail \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-197">LetAppsAccessEmail\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-198">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-199">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-200">LetAppsAccessEmail \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-200">LetAppsAccessEmail\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-201">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-202">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-203">LetAppsAccessEmail \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-203">LetAppsAccessEmail\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessemail-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-206">LetAppsAccessLocation</span><span class="sxs-lookup"><span data-stu-id="8ca71-206">LetAppsAccessLocation</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-207">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-208">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-209">LetAppsAccessLocation \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-209">LetAppsAccessLocation\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-211">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-212">LetAppsAccessLocation \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-212">LetAppsAccessLocation\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-213">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-214">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-215">LetAppsAccessLocation \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-215">LetAppsAccessLocation\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesslocation-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-216">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-217">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-218">LetAppsAccessMessaging</span><span class="sxs-lookup"><span data-stu-id="8ca71-218">LetAppsAccessMessaging</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-219">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-221">LetAppsAccessMessaging \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-221">LetAppsAccessMessaging\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-223">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-224">LetAppsAccessMessaging \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-224">LetAppsAccessMessaging\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-226">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-227">LetAppsAccessMessaging \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-227">LetAppsAccessMessaging\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmessaging-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-228">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-229">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-230">LetAppsAccessMicrophone</span><span class="sxs-lookup"><span data-stu-id="8ca71-230">LetAppsAccessMicrophone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-231">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-231">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-232">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-232">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-233">LetAppsAccessMicrophone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-233">LetAppsAccessMicrophone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-234">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-234">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-235">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-236">LetAppsAccessMicrophone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-236">LetAppsAccessMicrophone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-238">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-238">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-239">LetAppsAccessMicrophone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-239">LetAppsAccessMicrophone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmicrophone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-240">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-241">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-241">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-242">LetAppsAccessMotion</span><span class="sxs-lookup"><span data-stu-id="8ca71-242">LetAppsAccessMotion</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-243">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-243">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-244">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-244">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-245">LetAppsAccessMotion \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-245">LetAppsAccessMotion\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-246">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-246">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-247">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-247">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-248">LetAppsAccessMotion \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-248">LetAppsAccessMotion\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-249">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-250">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-250">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-251">LetAppsAccessMotion \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-251">LetAppsAccessMotion\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessmotion-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-252">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-253">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-253">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-254">LetAppsAccessNotifications</span><span class="sxs-lookup"><span data-stu-id="8ca71-254">LetAppsAccessNotifications</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-255">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-255">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-256">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-256">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-257">LetAppsAccessNotifications \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-257">LetAppsAccessNotifications\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-258">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-258">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-259">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-259">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-260">LetAppsAccessNotifications \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-260">LetAppsAccessNotifications\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-262">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-262">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-263">LetAppsAccessNotifications \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-263">LetAppsAccessNotifications\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessnotifications-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-264">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-265">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-266">LetAppsAccessPhone</span><span class="sxs-lookup"><span data-stu-id="8ca71-266">LetAppsAccessPhone</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-267">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-267">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-268">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-268">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-269">LetAppsAccessPhone \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-269">LetAppsAccessPhone\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-270">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-271">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-271">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-272">LetAppsAccessPhone \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-272">LetAppsAccessPhone\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-273">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-273">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-274">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-274">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-275">LetAppsAccessPhone \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-275">LetAppsAccessPhone\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessphone-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-276">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-277">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-277">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-278">LetAppsAccessRadios</span><span class="sxs-lookup"><span data-stu-id="8ca71-278">LetAppsAccessRadios</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-279">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-279">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-280">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-280">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-281">LetAppsAccessRadios \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-281">LetAppsAccessRadios\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-282">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-282">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-283">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-283">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-284">LetAppsAccessRadios \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-284">LetAppsAccessRadios\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-285">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-285">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-286">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-286">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-287">LetAppsAccessRadios \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-287">LetAppsAccessRadios\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccessradios-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-288">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-289">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-289">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-290">LetAppsAccessTasks</span><span class="sxs-lookup"><span data-stu-id="8ca71-290">LetAppsAccessTasks</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-291">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-291">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-292">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-292">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-293">LetAppsAccessTasks \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-293">LetAppsAccessTasks\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-294">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-295">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-295">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-296">LetAppsAccessTasks \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-296">LetAppsAccessTasks\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-297">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-298">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-298">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-299">LetAppsAccessTasks \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-299">LetAppsAccessTasks\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstasks-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-300">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-300">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-301">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-301">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-302">LetAppsAccessTrustedDevices</span><span class="sxs-lookup"><span data-stu-id="8ca71-302">LetAppsAccessTrustedDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-303">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-303">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-304">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-304">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-305">LetAppsAccessTrustedDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-305">LetAppsAccessTrustedDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-306">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-306">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-307">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-307">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-308">LetAppsAccessTrustedDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-308">LetAppsAccessTrustedDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-309">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-310">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-310">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-311">LetAppsAccessTrustedDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-311">LetAppsAccessTrustedDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsaccesstrusteddevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-313">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-313">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-314">LetAppsGetDiagnosticInfo</span><span class="sxs-lookup"><span data-stu-id="8ca71-314">LetAppsGetDiagnosticInfo</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-315">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-315">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-316">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-316">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-317">LetAppsGetDiagnosticInfo \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-317">LetAppsGetDiagnosticInfo\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-318">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-319">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-319">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-320">LetAppsGetDiagnosticInfo \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-320">LetAppsGetDiagnosticInfo\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-321">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-322">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-322">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-323">LetAppsGetDiagnosticInfo \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-323">LetAppsGetDiagnosticInfo\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsgetdiagnosticinfo-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-325">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-325">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-326">LetAppsRunInBackground</span><span class="sxs-lookup"><span data-stu-id="8ca71-326">LetAppsRunInBackground</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-327">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-327">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-328">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-328">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-329">LetAppsRunInBackground \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-329">LetAppsRunInBackground\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-330">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-331">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-331">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-332">LetAppsRunInBackground \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-332">LetAppsRunInBackground\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-334">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-334">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-335">LetAppsRunInBackground \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-335">LetAppsRunInBackground\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappsruninbackground-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-336">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-337">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-337">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-338">LetAppsSyncWithDevices</span><span class="sxs-lookup"><span data-stu-id="8ca71-338">LetAppsSyncWithDevices</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-339">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-339">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-340">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-340">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-341">LetAppsSyncWithDevices \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-341">LetAppsSyncWithDevices\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-342">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-343">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-343">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-344">LetAppsSyncWithDevices \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-344">LetAppsSyncWithDevices\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-345">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-345">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-346">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-346">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8ca71-347">LetAppsSyncWithDevices \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="8ca71-347">LetAppsSyncWithDevices\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-letappssyncwithdevices-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-348">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-348">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-349">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-349">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ca71-350">**ID**</span><span class="sxs-lookup"><span data-stu-id="8ca71-350">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-351">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ca71-351">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-352">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8ca71-352">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-353">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8ca71-353">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8ca71-354">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="8ca71-354">Describes the full path to the parent node.</span></span> <span data-ttu-id="8ca71-355">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="8ca71-355">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="8ca71-356">PublishUserActivities</span><span class="sxs-lookup"><span data-stu-id="8ca71-356">PublishUserActivities</span></span>](/windows/client-management/mdm/policy-csp-privacy#privacy-publishuseractivities)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ca71-357">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="8ca71-357">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8ca71-358">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8ca71-358">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ca71-359">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ca71-359">Requirements</span></span>



| <span data-ttu-id="8ca71-360">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ca71-360">Requirement</span></span> | <span data-ttu-id="8ca71-361">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ca71-361">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca71-362">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ca71-362">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca71-363">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ca71-363">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ca71-364">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ca71-364">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca71-365">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ca71-365">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8ca71-366">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ca71-366">Namespace</span></span><br/>                | <span data-ttu-id="8ca71-367">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="8ca71-367">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8ca71-368">MOF</span><span class="sxs-lookup"><span data-stu-id="8ca71-368">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ca71-369"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ca71-369"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ca71-370">DLL</span><span class="sxs-lookup"><span data-stu-id="8ca71-370">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ca71-371"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ca71-371"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca71-372">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ca71-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca71-373">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="8ca71-373">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

