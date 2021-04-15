---
title: Classe MDM_Policy_Config01_LockDown02
description: La \_ classe Config01 Lockdown02 de la stratégie MDM \_ \_ représente les stratégies de verrouillage disponibles.
ms.assetid: 1d744400-70db-4f6b-97d0-7799fdfda44f
keywords:
- Classe MDM_Policy_Config01_LockDown02
- Classe MDM_Policy_Config01_LockDown02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LockDown02
- MDM_Policy_Config01_LockDown02.InstanceID
- MDM_Policy_Config01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf9914573c1a3f693d88da8b35b2d577e1f21f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465239"
---
# <a name="mdm_policy_config01_lockdown02-class"></a><span data-ttu-id="fffca-105">\_Classe LockDown02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="fffca-105">MDM\_Policy\_Config01\_LockDown02 class</span></span>

<span data-ttu-id="fffca-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="fffca-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fffca-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="fffca-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fffca-108">La **classe \_ \_ Config01 \_ Lockdown02 de la stratégie MDM** représente les stratégies de verrouillage disponibles.</span><span class="sxs-lookup"><span data-stu-id="fffca-108">The **MDM\_Policy\_Config01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="fffca-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="fffca-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fffca-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fffca-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="fffca-111">Membres</span><span class="sxs-lookup"><span data-stu-id="fffca-111">Members</span></span>

<span data-ttu-id="fffca-112">La **classe \_ \_ Config01 \_ LockDown02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="fffca-112">The **MDM\_Policy\_Config01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="fffca-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fffca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fffca-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fffca-114">Properties</span></span>

<span data-ttu-id="fffca-115">La **classe \_ \_ Config01 \_ LockDown02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="fffca-115">The **MDM\_Policy\_Config01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fffca-116">AllowEdgeSwipe</span><span class="sxs-lookup"><span data-stu-id="fffca-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffca-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="fffca-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fffca-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="fffca-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fffca-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fffca-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffca-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fffca-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffca-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fffca-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffca-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fffca-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fffca-123">Identifie le nom du nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fffca-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="fffca-124">Pour cette classe, la chaîne est « Lockdown ».</span><span class="sxs-lookup"><span data-stu-id="fffca-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="fffca-125">**ID**</span><span class="sxs-lookup"><span data-stu-id="fffca-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fffca-126">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fffca-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fffca-127">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="fffca-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fffca-128">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fffca-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fffca-129">Décrit le chemin d’accès complet au nœud parent.</span><span class="sxs-lookup"><span data-stu-id="fffca-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fffca-130">Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Config »</span><span class="sxs-lookup"><span data-stu-id="fffca-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fffca-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fffca-131">Requirements</span></span>



| <span data-ttu-id="fffca-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fffca-132">Requirement</span></span> | <span data-ttu-id="fffca-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="fffca-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fffca-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffca-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fffca-135">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fffca-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fffca-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffca-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fffca-137">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fffca-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="fffca-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fffca-138">Namespace</span></span><br/>                | <span data-ttu-id="fffca-139">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="fffca-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="fffca-140">MOF</span><span class="sxs-lookup"><span data-stu-id="fffca-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fffca-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fffca-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="fffca-142">DLL</span><span class="sxs-lookup"><span data-stu-id="fffca-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fffca-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="fffca-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

