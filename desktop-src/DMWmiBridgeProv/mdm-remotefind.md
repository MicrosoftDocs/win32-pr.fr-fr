---
title: Classe MDM_RemoteFind
description: La \_ classe REMOTEFIND MDM récupère les informations d’emplacement pour un appareil particulier.
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- Classe MDM_RemoteFind
- Classe MDM_RemoteFind, Description
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740076"
---
# <a name="mdm_remotefind-class"></a><span data-ttu-id="d908a-105">\_Classe REMOTEFIND MDM</span><span class="sxs-lookup"><span data-stu-id="d908a-105">MDM\_RemoteFind class</span></span>

<span data-ttu-id="d908a-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d908a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d908a-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d908a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d908a-108">La **classe \_ RemoteFind MDM** récupère les informations d’emplacement pour un appareil particulier.</span><span class="sxs-lookup"><span data-stu-id="d908a-108">The **MDM\_RemoteFind** class retrieves the location information for a particular device.</span></span>

<span data-ttu-id="d908a-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d908a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d908a-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d908a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a><span data-ttu-id="d908a-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d908a-111">Members</span></span>

<span data-ttu-id="d908a-112">La **classe \_ RemoteFind MDM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d908a-112">The **MDM\_RemoteFind** class has these types of members:</span></span>

-   [<span data-ttu-id="d908a-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d908a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d908a-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d908a-114">Properties</span></span>

<span data-ttu-id="d908a-115">La **classe \_ RemoteFind MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d908a-115">The **MDM\_RemoteFind** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d908a-116">DesiredAccuracy</span><span class="sxs-lookup"><span data-stu-id="d908a-116">DesiredAccuracy</span></span>](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d908a-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d908a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d908a-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d908a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d908a-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d908a-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d908a-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d908a-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d908a-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d908a-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d908a-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d908a-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d908a-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d908a-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="d908a-124">Pour cette classe, la chaîne est « RemoteFind ».</span><span class="sxs-lookup"><span data-stu-id="d908a-124">For this class, the string is "RemoteFind".</span></span>

</dd> <dt>

[<span data-ttu-id="d908a-125">Maximum</span><span class="sxs-lookup"><span data-stu-id="d908a-125">MaximumAge</span></span>](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d908a-126">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d908a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d908a-127">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d908a-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d908a-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="d908a-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d908a-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d908a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d908a-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d908a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d908a-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d908a-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d908a-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d908a-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="d908a-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/ »</span><span class="sxs-lookup"><span data-stu-id="d908a-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> <dt>

[<span data-ttu-id="d908a-134">Délai d'expiration</span><span class="sxs-lookup"><span data-stu-id="d908a-134">Timeout</span></span>](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d908a-135">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d908a-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d908a-136">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d908a-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d908a-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d908a-137">Requirements</span></span>



| <span data-ttu-id="d908a-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d908a-138">Requirement</span></span> | <span data-ttu-id="d908a-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d908a-139">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d908a-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d908a-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d908a-141">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d908a-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d908a-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d908a-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d908a-143">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d908a-143">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="d908a-144">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d908a-144">Namespace</span></span><br/>                | <span data-ttu-id="d908a-145">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d908a-145">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                              |
| <span data-ttu-id="d908a-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d908a-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d908a-147"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d908a-147"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="d908a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d908a-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d908a-149"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d908a-149"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d908a-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d908a-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d908a-151">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d908a-151">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

