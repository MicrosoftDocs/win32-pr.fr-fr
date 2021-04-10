---
title: Classe MDM_Policy_Result01_Cellular02
description: la \_ classe Result01 Cellular02 de la stratégie MDM \_ \_ représente les stratégies cellulaires.
ms.assetid: df2b2461-5e4e-4b28-87f1-5ca348409192
keywords:
- Classe MDM_Policy_Result01_Cellular02
- Classe MDM_Policy_Result01_Cellular02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cellular02
- MDM_Policy_Result01_Cellular02.InstanceID
- MDM_Policy_Result01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f2a8b9178ecd4d69b0c313eb7fdcb826e944317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103121"
---
# <a name="mdm_policy_result01_cellular02-class"></a><span data-ttu-id="680e3-105">\_Classe Cellular02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="680e3-105">MDM\_Policy\_Result01\_Cellular02 class</span></span>

<span data-ttu-id="680e3-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="680e3-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="680e3-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="680e3-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="680e3-108">la \_ classe Result01 Cellular02 de la stratégie MDM \_ \_ représente les stratégies cellulaires.</span><span class="sxs-lookup"><span data-stu-id="680e3-108">the MDM\_Policy\_Result01\_Cellular02 class represents the cellular policies.</span></span>

<span data-ttu-id="680e3-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="680e3-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="680e3-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="680e3-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="680e3-111">Membres</span><span class="sxs-lookup"><span data-stu-id="680e3-111">Members</span></span>

<span data-ttu-id="680e3-112">La **classe \_ \_ Result01 \_ Cellular02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="680e3-112">The **MDM\_Policy\_Result01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="680e3-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="680e3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="680e3-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="680e3-114">Properties</span></span>

<span data-ttu-id="680e3-115">La **classe \_ \_ Result01 \_ Cellular02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="680e3-115">The **MDM\_Policy\_Result01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="680e3-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="680e3-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="680e3-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="680e3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="680e3-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="680e3-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="680e3-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="680e3-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-121">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="680e3-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-122">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="680e3-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="680e3-123">LetAppsAccessCellularData \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="680e3-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="680e3-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-125">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="680e3-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="680e3-126">LetAppsAccessCellularData \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="680e3-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="680e3-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-128">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="680e3-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="680e3-129">LetAppsAccessCellularData \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="680e3-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-130">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="680e3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="680e3-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="680e3-132">**ID**</span><span class="sxs-lookup"><span data-stu-id="680e3-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="680e3-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="680e3-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="680e3-135">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="680e3-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="680e3-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="680e3-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="680e3-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="680e3-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="680e3-138">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="680e3-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="680e3-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="680e3-139">Requirements</span></span>



| <span data-ttu-id="680e3-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="680e3-140">Requirement</span></span> | <span data-ttu-id="680e3-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="680e3-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="680e3-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680e3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="680e3-143">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="680e3-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="680e3-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="680e3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="680e3-145">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="680e3-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="680e3-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="680e3-146">Namespace</span></span><br/>                | <span data-ttu-id="680e3-147">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="680e3-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="680e3-148">MOF</span><span class="sxs-lookup"><span data-stu-id="680e3-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="680e3-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="680e3-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="680e3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="680e3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="680e3-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="680e3-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

