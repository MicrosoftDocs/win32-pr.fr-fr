---
title: Classe MDM_Policy_Result01_ApplicationManagement02
description: La \_ classe Result01 ApplicationManagement02 de la stratégie MDM \_ \_ représente les stratégies de gestion des applications disponibles. \_ \_ \_ La classe ApplicationManagement02 de la stratégie MDM Result01 représente les stratégies de gestion des applications disponibles.
ms.assetid: 141614e4-b2b1-49d9-879c-f6f86bee070c
keywords:
- Classe MDM_Policy_Result01_ApplicationManagement02
- Classe MDM_Policy_Result01_ApplicationManagement02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationManagement02
- MDM_Policy_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 477e4e58216c912aa14ec17b8e5879643e3de83f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103879"
---
# <a name="mdm_policy_result01_applicationmanagement02-class"></a><span data-ttu-id="de33a-105">\_Classe ApplicationManagement02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="de33a-105">MDM\_Policy\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="de33a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="de33a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="de33a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="de33a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="de33a-108">La **classe \_ \_ Result01 \_ ApplicationManagement02 de la stratégie MDM** représente les stratégies de gestion des applications disponibles.</span><span class="sxs-lookup"><span data-stu-id="de33a-108">The **MDM\_Policy\_Result01\_ApplicationManagement02** class represents the application management policies available.</span></span>

<span data-ttu-id="de33a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="de33a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de33a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de33a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a><span data-ttu-id="de33a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="de33a-111">Members</span></span>

<span data-ttu-id="de33a-112">La **classe \_ \_ Result01 \_ ApplicationManagement02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="de33a-112">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="de33a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de33a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de33a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="de33a-114">Properties</span></span>

<span data-ttu-id="de33a-115">La **classe \_ \_ Result01 \_ ApplicationManagement02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="de33a-115">The **MDM\_Policy\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="de33a-116">AllowAllTrustedApps</span><span class="sxs-lookup"><span data-stu-id="de33a-116">AllowAllTrustedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de33a-119">AllowAppStoreAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="de33a-119">AllowAppStoreAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de33a-122">AllowDeveloperUnlock</span><span class="sxs-lookup"><span data-stu-id="de33a-122">AllowDeveloperUnlock</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-123">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-124">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de33a-125">AllowGameDVR</span><span class="sxs-lookup"><span data-stu-id="de33a-125">AllowGameDVR</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de33a-128">AllowSharedUserAppData</span><span class="sxs-lookup"><span data-stu-id="de33a-128">AllowSharedUserAppData</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de33a-131">DisableStoreOriginatedApps</span><span class="sxs-lookup"><span data-stu-id="de33a-131">DisableStoreOriginatedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-132">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-133">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="de33a-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="de33a-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de33a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de33a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de33a-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de33a-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de33a-138">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="de33a-138">Identifies the name of the parent node.</span></span> <span data-ttu-id="de33a-139">Pour cette classe, la chaîne est « ApplicationManagement ».</span><span class="sxs-lookup"><span data-stu-id="de33a-139">For this class, the string is "ApplicationManagement".</span></span>

</dd> <dt>

<span data-ttu-id="de33a-140">**ID**</span><span class="sxs-lookup"><span data-stu-id="de33a-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="de33a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="de33a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de33a-143">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="de33a-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="de33a-144">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="de33a-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="de33a-145">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="de33a-145">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="de33a-146">RestrictAppDataToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="de33a-146">RestrictAppDataToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-147">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="de33a-149">RestrictAppToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="de33a-149">RestrictAppToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="de33a-150">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="de33a-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="de33a-151">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="de33a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="de33a-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de33a-152">Requirements</span></span>



| <span data-ttu-id="de33a-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de33a-153">Requirement</span></span> | <span data-ttu-id="de33a-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="de33a-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de33a-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de33a-155">Minimum supported client</span></span><br/> | <span data-ttu-id="de33a-156">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de33a-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="de33a-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de33a-157">Minimum supported server</span></span><br/> | <span data-ttu-id="de33a-158">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="de33a-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="de33a-159">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de33a-159">Namespace</span></span><br/>                | <span data-ttu-id="de33a-160">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="de33a-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="de33a-161">MOF</span><span class="sxs-lookup"><span data-stu-id="de33a-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de33a-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de33a-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="de33a-163">DLL</span><span class="sxs-lookup"><span data-stu-id="de33a-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de33a-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de33a-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de33a-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de33a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de33a-166">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="de33a-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

