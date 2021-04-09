---
title: Classe MDM_Policy_Result01_WindowsInkWorkspace02
description: La \_ \_ classe Result01 WindowsInkWorkspace02 de la stratégie MDM \_ représente les stratégies de l’espace de travail Ink disponibles.
ms.assetid: a3bb85e5-554f-4f41-8e65-e221f8adc947
keywords:
- Classe MDM_Policy_Result01_WindowsInkWorkspace02
- Classe MDM_Policy_Result01_WindowsInkWorkspace02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsInkWorkspace02
- MDM_Policy_Result01_WindowsInkWorkspace02.InstanceID
- MDM_Policy_Result01_WindowsInkWorkspace02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d64100ec0566b7cd996840d012d018b8dbc75aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843129"
---
# <a name="mdm_policy_result01_windowsinkworkspace02-class"></a><span data-ttu-id="69888-105">\_Classe WindowsInkWorkspace02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="69888-105">MDM\_Policy\_Result01\_WindowsInkWorkspace02 class</span></span>

<span data-ttu-id="69888-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="69888-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="69888-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="69888-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="69888-108">La [**classe \_ \_ Result01 \_ WindowsInkWorkspace02 de la stratégie MDM**](mdm-policy-config01-windowsinkworkspace02.md) représente les stratégies de l’espace de travail Ink disponibles.</span><span class="sxs-lookup"><span data-stu-id="69888-108">The [**MDM\_Policy\_Result01\_WindowsInkWorkspace02**](mdm-policy-config01-windowsinkworkspace02.md) class represents the ink workspace policies available.</span></span>

<span data-ttu-id="69888-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="69888-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="69888-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69888-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsInkWorkspace02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsInkWorkspace;
  sint32 AllowSuggestedAppsInWindowsInkWorkspace;
};
```

## <a name="members"></a><span data-ttu-id="69888-111">Membres</span><span class="sxs-lookup"><span data-stu-id="69888-111">Members</span></span>

<span data-ttu-id="69888-112">La **classe \_ \_ Result01 \_ WindowsInkWorkspace02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="69888-112">The **MDM\_Policy\_Result01\_WindowsInkWorkspace02** class has these types of members:</span></span>

-   [<span data-ttu-id="69888-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69888-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69888-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="69888-114">Properties</span></span>

<span data-ttu-id="69888-115">La **classe \_ \_ Result01 \_ WindowsInkWorkspace02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="69888-115">The **MDM\_Policy\_Result01\_WindowsInkWorkspace02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="69888-116">AllowSuggestedAppsInWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="69888-116">AllowSuggestedAppsInWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowsuggestedappsinwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="69888-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="69888-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="69888-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69888-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="69888-119">AllowWindowsInkWorkspace</span><span class="sxs-lookup"><span data-stu-id="69888-119">AllowWindowsInkWorkspace</span></span>](/windows/client-management/mdm/policy-csp-windowsinkworkspace#windowsinkworkspace-allowwindowsinkworkspace)
</dt> <dd> <dl> <dt>

<span data-ttu-id="69888-120">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="69888-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="69888-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="69888-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="69888-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="69888-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69888-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="69888-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69888-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69888-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69888-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="69888-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="69888-126">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="69888-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="69888-127">Pour cette classe, la chaîne est « WindowsInkWorkspace ».</span><span class="sxs-lookup"><span data-stu-id="69888-127">For this class, the string is "WindowsInkWorkspace".</span></span>

</dd> <dt>

<span data-ttu-id="69888-128">**ID**</span><span class="sxs-lookup"><span data-stu-id="69888-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69888-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="69888-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69888-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="69888-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69888-131">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="69888-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="69888-132">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="69888-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="69888-133">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="69888-133">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69888-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69888-134">Requirements</span></span>



| <span data-ttu-id="69888-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69888-135">Requirement</span></span> | <span data-ttu-id="69888-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="69888-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69888-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69888-137">Minimum supported client</span></span><br/> | <span data-ttu-id="69888-138">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69888-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="69888-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69888-139">Minimum supported server</span></span><br/> | <span data-ttu-id="69888-140">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="69888-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="69888-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="69888-141">Namespace</span></span><br/>                | <span data-ttu-id="69888-142">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="69888-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="69888-143">MOF</span><span class="sxs-lookup"><span data-stu-id="69888-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69888-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69888-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="69888-145">DLL</span><span class="sxs-lookup"><span data-stu-id="69888-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69888-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="69888-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

