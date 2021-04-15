---
title: Classe MDM_Policy_Result01_LockDown02
description: La \_ classe Result01 Lockdown02 de la stratégie MDM \_ \_ représente les stratégies de verrouillage disponibles.
ms.assetid: 78eab50e-b1a7-4b96-a848-b8a86a3b82c3
keywords:
- Classe MDM_Policy_Result01_LockDown02
- Classe MDM_Policy_Result01_LockDown02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_LockDown02
- MDM_Policy_Result01_LockDown02.InstanceID
- MDM_Policy_Result01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 159e2178e3e5600bef4fc366a0cf49b7856ce886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465011"
---
# <a name="mdm_policy_result01_lockdown02-class"></a><span data-ttu-id="d7ead-105">\_Classe LockDown02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="d7ead-105">MDM\_Policy\_Result01\_LockDown02 class</span></span>

<span data-ttu-id="d7ead-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d7ead-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d7ead-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d7ead-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d7ead-108">La **classe \_ \_ Result01 \_ Lockdown02 de la stratégie MDM** représente les stratégies de verrouillage disponibles.</span><span class="sxs-lookup"><span data-stu-id="d7ead-108">The **MDM\_Policy\_Result01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="d7ead-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="d7ead-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ead-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7ead-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="d7ead-111">Membres</span><span class="sxs-lookup"><span data-stu-id="d7ead-111">Members</span></span>

<span data-ttu-id="d7ead-112">La **classe \_ \_ Result01 \_ LockDown02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d7ead-112">The **MDM\_Policy\_Result01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="d7ead-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7ead-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d7ead-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d7ead-114">Properties</span></span>

<span data-ttu-id="d7ead-115">La **classe \_ \_ Result01 \_ LockDown02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d7ead-115">The **MDM\_Policy\_Result01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d7ead-116">AllowEdgeSwipe</span><span class="sxs-lookup"><span data-stu-id="d7ead-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7ead-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="d7ead-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d7ead-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d7ead-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d7ead-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d7ead-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7ead-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d7ead-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7ead-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d7ead-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7ead-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7ead-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7ead-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d7ead-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="d7ead-124">Pour cette classe, la chaîne est « Lockdown ».</span><span class="sxs-lookup"><span data-stu-id="d7ead-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="d7ead-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="d7ead-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d7ead-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d7ead-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d7ead-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d7ead-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d7ead-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d7ead-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d7ead-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="d7ead-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="d7ead-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »</span><span class="sxs-lookup"><span data-stu-id="d7ead-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7ead-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7ead-131">Requirements</span></span>



| <span data-ttu-id="d7ead-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7ead-132">Requirement</span></span> | <span data-ttu-id="d7ead-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7ead-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ead-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ead-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ead-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7ead-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d7ead-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ead-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ead-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7ead-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="d7ead-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d7ead-138">Namespace</span></span><br/>                | <span data-ttu-id="d7ead-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d7ead-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="d7ead-140">MOF</span><span class="sxs-lookup"><span data-stu-id="d7ead-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d7ead-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d7ead-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="d7ead-142">DLL</span><span class="sxs-lookup"><span data-stu-id="d7ead-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7ead-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="d7ead-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

