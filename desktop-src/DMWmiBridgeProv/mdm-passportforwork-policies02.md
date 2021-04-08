---
title: Classe MDM_PassportForWork_Policies02
description: La \_ classe POLICIES02 MDM PassportForWork configure \_ Windows Hello entreprise.
ms.assetid: 362fe819-a68a-4433-8b43-201d9678a8da
keywords:
- Classe MDM_PassportForWork_Policies02
- Classe MDM_PassportForWork_Policies02, Description
topic_type:
- apiref
api_name:
- MDM_PassportForWork_Policies02
- MDM_PassportForWork_Policies02.InstanceID
- MDM_PassportForWork_Policies02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fdf407289f93f5ecff0e57ebf7b7fa8d9844183
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941934"
---
# <a name="mdm_passportforwork_policies02-class"></a><span data-ttu-id="52283-105">\_ \_ Classe POLICIES02 PassportForWork MDM</span><span class="sxs-lookup"><span data-stu-id="52283-105">MDM\_PassportForWork\_Policies02 class</span></span>

<span data-ttu-id="52283-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="52283-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="52283-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="52283-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="52283-108">La **classe \_ \_ Policies02 MDM PassportForWork** configure Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="52283-108">The **MDM\_PassportForWork\_Policies02** class provisions Windows Hello for Business.</span></span>

<span data-ttu-id="52283-109">La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="52283-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="52283-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52283-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_Policies02
{
  string  InstanceID;
  string  ParentID;
  boolean UsePassportForWork;
  boolean RequireSecurityDevice;
};
```

## <a name="members"></a><span data-ttu-id="52283-111">Membres</span><span class="sxs-lookup"><span data-stu-id="52283-111">Members</span></span>

<span data-ttu-id="52283-112">La **classe \_ PassportForWork \_ Policies02 MDM** contient les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="52283-112">The **MDM\_PassportForWork\_Policies02** class has these types of members:</span></span>

-   [<span data-ttu-id="52283-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52283-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="52283-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="52283-114">Properties</span></span>

<span data-ttu-id="52283-115">La **classe \_ PassportForWork \_ Policies02 MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="52283-115">The **MDM\_PassportForWork\_Policies02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="52283-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="52283-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52283-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52283-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52283-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52283-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52283-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52283-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="52283-120">Nœud racine pour les stratégies Windows Hello entreprise.</span><span class="sxs-lookup"><span data-stu-id="52283-120">Root node for Windows Hello for Business policies.</span></span>

</dd> <dt>

<span data-ttu-id="52283-121">**ID**</span><span class="sxs-lookup"><span data-stu-id="52283-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="52283-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="52283-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="52283-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="52283-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="52283-124">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="52283-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="52283-125">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="52283-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="52283-126">Pour cette classe, la chaîne est « ./Vendor/MSFT/PassPortForWork/*TenantID*»</span><span class="sxs-lookup"><span data-stu-id="52283-126">For this class, the string is "./Vendor/MSFT/PassPortForWork/*TenantID*"</span></span>

</dd> <dt>

[<span data-ttu-id="52283-127">RequireSecurityDevice</span><span class="sxs-lookup"><span data-stu-id="52283-127">RequireSecurityDevice</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-requiresecuritydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52283-128">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="52283-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52283-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52283-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="52283-130">UsePassportForWork</span><span class="sxs-lookup"><span data-stu-id="52283-130">UsePassportForWork</span></span>](/windows/client-management/mdm/passportforwork-csp#tenantid-policies-usepassportforwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="52283-131">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="52283-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="52283-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="52283-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="52283-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52283-133">Requirements</span></span>



| <span data-ttu-id="52283-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52283-134">Requirement</span></span> | <span data-ttu-id="52283-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="52283-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="52283-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52283-136">Minimum supported client</span></span><br/> | <span data-ttu-id="52283-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52283-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="52283-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52283-138">Minimum supported server</span></span><br/> | <span data-ttu-id="52283-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="52283-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="52283-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="52283-140">Namespace</span></span><br/>                | <span data-ttu-id="52283-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="52283-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="52283-142">MOF</span><span class="sxs-lookup"><span data-stu-id="52283-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="52283-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="52283-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="52283-144">DLL</span><span class="sxs-lookup"><span data-stu-id="52283-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52283-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52283-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52283-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52283-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52283-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="52283-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

