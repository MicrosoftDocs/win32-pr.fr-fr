---
title: Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02
description: La \_ classe Result01 WindowsDefenderSecurityCenter02 de la stratégie MDM \_ \_ représente les stratégies Windows Defender Security Center.
ms.assetid: 59047e16-a188-4ec9-9d1b-db2b15c1109b
keywords:
- Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- Classe MDM_Policy_Result01_WindowsDefenderSecurityCenter02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7739410347169637ca5f27fef5627e26f8347c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464371"
---
# <a name="mdm_policy_result01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="3cdcc-105">\_Classe WindowsDefenderSecurityCenter02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="3cdcc-105">MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="3cdcc-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3cdcc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3cdcc-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3cdcc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3cdcc-108">La \_ classe Result01 WindowsDefenderSecurityCenter02 de la stratégie MDM \_ \_ représente les stratégies Windows Defender Security Center.</span><span class="sxs-lookup"><span data-stu-id="3cdcc-108">The MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="3cdcc-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3cdcc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cdcc-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cdcc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="3cdcc-111">Membres</span><span class="sxs-lookup"><span data-stu-id="3cdcc-111">Members</span></span>

<span data-ttu-id="3cdcc-112">La **classe \_ \_ Result01 \_ WindowsDefenderSecurityCenter02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3cdcc-112">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="3cdcc-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3cdcc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cdcc-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3cdcc-114">Properties</span></span>

<span data-ttu-id="3cdcc-115">La **classe \_ \_ Result01 \_ WindowsDefenderSecurityCenter02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3cdcc-115">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3cdcc-116">Prennent</span><span class="sxs-lookup"><span data-stu-id="3cdcc-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="3cdcc-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="3cdcc-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="3cdcc-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="3cdcc-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="3cdcc-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="3cdcc-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="3cdcc-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-138">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="3cdcc-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-141">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-143">E-mail</span><span class="sxs-lookup"><span data-stu-id="3cdcc-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-145">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="3cdcc-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="3cdcc-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3cdcc-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3cdcc-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-155">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3cdcc-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3cdcc-156">**ID**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3cdcc-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-159">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3cdcc-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-160">Numéros</span><span class="sxs-lookup"><span data-stu-id="3cdcc-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-161">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-162">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3cdcc-163">URL</span><span class="sxs-lookup"><span data-stu-id="3cdcc-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cdcc-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3cdcc-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3cdcc-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3cdcc-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3cdcc-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cdcc-166">Requirements</span></span>



| <span data-ttu-id="3cdcc-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cdcc-167">Requirement</span></span> | <span data-ttu-id="3cdcc-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cdcc-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cdcc-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cdcc-169">Minimum supported client</span></span><br/> | <span data-ttu-id="3cdcc-170">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3cdcc-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3cdcc-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cdcc-171">Minimum supported server</span></span><br/> | <span data-ttu-id="3cdcc-172">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3cdcc-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3cdcc-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3cdcc-173">Namespace</span></span><br/>                | <span data-ttu-id="3cdcc-174">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3cdcc-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3cdcc-175">MOF</span><span class="sxs-lookup"><span data-stu-id="3cdcc-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cdcc-176"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cdcc-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cdcc-177">DLL</span><span class="sxs-lookup"><span data-stu-id="3cdcc-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cdcc-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cdcc-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

