---
title: Classe MDM_AppLocker_MSI03
description: La \_ \_ classe MSI03 de MDM AppLocker définit les restrictions de stratégie pour le traitement des fichiers msi.
ms.assetid: b7b6602d-38b7-46f0-9542-71228ab0c303
keywords:
- Classe MDM_AppLocker_MSI03
- Classe MDM_AppLocker_MSI03, Description
topic_type:
- apiref
api_name:
- MDM_AppLocker_MSI03
- MDM_AppLocker_MSI03.InstanceID
- MDM_AppLocker_MSI03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5bd17a979ac0e4a6dcbbc07a38ba72bfd50ede4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743565"
---
# <a name="mdm_applocker_msi03-class"></a><span data-ttu-id="e01f7-105">\_ \_ Classe MSI03 de MDM AppLocker</span><span class="sxs-lookup"><span data-stu-id="e01f7-105">MDM\_AppLocker\_MSI03 class</span></span>

<span data-ttu-id="e01f7-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="e01f7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e01f7-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="e01f7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e01f7-108">La **classe \_ \_ MSI03 de MDM AppLocker** définit les restrictions de stratégie pour le traitement des fichiers msi.</span><span class="sxs-lookup"><span data-stu-id="e01f7-108">The **MDM\_AppLocker\_MSI03** class defines the policy restrictions for processing MSI files.</span></span>

<span data-ttu-id="e01f7-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="e01f7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01f7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e01f7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_MSI03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="e01f7-111">Membres</span><span class="sxs-lookup"><span data-stu-id="e01f7-111">Members</span></span>

<span data-ttu-id="e01f7-112">La **classe \_ \_ MSI03 de MDM AppLocker** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e01f7-112">The **MDM\_AppLocker\_MSI03** class has these types of members:</span></span>

-   [<span data-ttu-id="e01f7-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e01f7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e01f7-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e01f7-114">Properties</span></span>

<span data-ttu-id="e01f7-115">La **classe \_ \_ MSI03 de MDM AppLocker** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e01f7-115">The **MDM\_AppLocker\_MSI03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e01f7-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="e01f7-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01f7-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e01f7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01f7-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e01f7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e01f7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e01f7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01f7-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e01f7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01f7-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e01f7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01f7-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e01f7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e01f7-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e01f7-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="e01f7-124">**ID**</span><span class="sxs-lookup"><span data-stu-id="e01f7-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01f7-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e01f7-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01f7-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e01f7-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e01f7-127">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e01f7-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e01f7-128">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="e01f7-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="e01f7-129">Pour cette classe, la chaîne est « ./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions »</span><span class="sxs-lookup"><span data-stu-id="e01f7-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="e01f7-130">**Stratégie**</span><span class="sxs-lookup"><span data-stu-id="e01f7-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e01f7-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e01f7-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e01f7-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e01f7-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e01f7-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e01f7-133">Requirements</span></span>



| <span data-ttu-id="e01f7-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e01f7-134">Requirement</span></span> | <span data-ttu-id="e01f7-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="e01f7-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e01f7-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e01f7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e01f7-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e01f7-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e01f7-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e01f7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e01f7-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e01f7-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e01f7-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e01f7-140">Namespace</span></span><br/>                | <span data-ttu-id="e01f7-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="e01f7-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e01f7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e01f7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e01f7-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e01f7-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e01f7-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e01f7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e01f7-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e01f7-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e01f7-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e01f7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e01f7-147">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="e01f7-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

