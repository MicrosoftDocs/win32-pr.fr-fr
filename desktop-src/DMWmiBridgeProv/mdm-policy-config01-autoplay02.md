---
title: Classe MDM_Policy_Config01_Autoplay02
description: La \_ classe Config01 Autoplay02 de la stratégie MDM \_ \_ configure les stratégies d’exécution automatique disponibles.
ms.assetid: ef7ccdb6-3f77-4c43-87d9-56acda97be21
keywords:
- Classe MDM_Policy_Config01_Autoplay02
- Classe MDM_Policy_Config01_Autoplay02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Autoplay02
- MDM_Policy_Config01_Autoplay02.InstanceID
- MDM_Policy_Config01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e064d0b0eed457bcafdf4da9bf8e72fbb4916e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032670"
---
# <a name="mdm_policy_config01_autoplay02-class"></a><span data-ttu-id="3b037-105">\_Classe Autoplay02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="3b037-105">MDM\_Policy\_Config01\_Autoplay02 class</span></span>

<span data-ttu-id="3b037-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="3b037-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3b037-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="3b037-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3b037-108">La \_ classe Config01 Autoplay02 de la stratégie MDM \_ \_ configure les stratégies d’exécution automatique disponibles.</span><span class="sxs-lookup"><span data-stu-id="3b037-108">The MDM\_Policy\_Config01\_Autoplay02 class configures the available autoplay policies.</span></span>

<span data-ttu-id="3b037-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="3b037-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b037-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b037-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="3b037-111">Membres</span><span class="sxs-lookup"><span data-stu-id="3b037-111">Members</span></span>

<span data-ttu-id="3b037-112">La **classe \_ \_ Config01 \_ Autoplay02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b037-112">The **MDM\_Policy\_Config01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="3b037-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b037-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3b037-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b037-114">Properties</span></span>

<span data-ttu-id="3b037-115">La **classe \_ \_ Config01 \_ Autoplay02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3b037-115">The **MDM\_Policy\_Config01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3b037-116">DisallowAutoplayForNonVolumeDevices</span><span class="sxs-lookup"><span data-stu-id="3b037-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b037-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b037-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b037-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b037-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b037-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3b037-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b037-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b037-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b037-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b037-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b037-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b037-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3b037-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="3b037-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b037-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b037-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b037-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b037-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3b037-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3b037-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b037-127">SetDefaultAutoRunBehavior</span><span class="sxs-lookup"><span data-stu-id="3b037-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b037-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b037-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b037-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b037-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3b037-130">TurnOffAutoPlay</span><span class="sxs-lookup"><span data-stu-id="3b037-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3b037-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3b037-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3b037-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3b037-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b037-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b037-133">Requirements</span></span>



| <span data-ttu-id="3b037-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b037-134">Requirement</span></span> | <span data-ttu-id="3b037-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b037-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b037-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b037-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3b037-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3b037-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3b037-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b037-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3b037-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b037-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3b037-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3b037-140">Namespace</span></span><br/>                | <span data-ttu-id="3b037-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="3b037-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3b037-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3b037-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3b037-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3b037-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3b037-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3b037-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b037-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b037-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

