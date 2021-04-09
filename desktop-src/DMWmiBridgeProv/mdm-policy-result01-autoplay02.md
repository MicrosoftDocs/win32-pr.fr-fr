---
title: Classe MDM_Policy_Result01_Autoplay02
description: La \_ classe Result01 Autoplay02 de la stratégie MDM \_ \_ représente les stratégies d’exécution automatique disponibles.
ms.assetid: f116015d-f10e-4d17-9c0b-7253894e6c0f
keywords:
- Classe MDM_Policy_Result01_Autoplay02
- Classe MDM_Policy_Result01_Autoplay02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02.InstanceID
- MDM_Policy_Result01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abf48754cff1513d6d373c9addb34b8ec9acc26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106129"
---
# <a name="mdm_policy_result01_autoplay02-class"></a><span data-ttu-id="21b33-105">\_Classe Autoplay02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="21b33-105">MDM\_Policy\_Result01\_Autoplay02 class</span></span>

<span data-ttu-id="21b33-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="21b33-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="21b33-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="21b33-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="21b33-108">La \_ classe Result01 Autoplay02 de la stratégie MDM \_ \_ représente les stratégies d’exécution automatique disponibles.</span><span class="sxs-lookup"><span data-stu-id="21b33-108">The MDM\_Policy\_Result01\_Autoplay02 class represents the available autoplay policies.</span></span>

<span data-ttu-id="21b33-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="21b33-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="21b33-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21b33-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="21b33-111">Membres</span><span class="sxs-lookup"><span data-stu-id="21b33-111">Members</span></span>

<span data-ttu-id="21b33-112">La **classe \_ \_ Result01 \_ Autoplay02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="21b33-112">The **MDM\_Policy\_Result01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="21b33-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21b33-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="21b33-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="21b33-114">Properties</span></span>

<span data-ttu-id="21b33-115">La **classe \_ \_ Result01 \_ Autoplay02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="21b33-115">The **MDM\_Policy\_Result01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="21b33-116">DisallowAutoplayForNonVolumeDevices</span><span class="sxs-lookup"><span data-stu-id="21b33-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21b33-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21b33-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21b33-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="21b33-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="21b33-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="21b33-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21b33-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21b33-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21b33-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21b33-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21b33-122">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="21b33-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="21b33-123">**ID**</span><span class="sxs-lookup"><span data-stu-id="21b33-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="21b33-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21b33-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21b33-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="21b33-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="21b33-126">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="21b33-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="21b33-127">SetDefaultAutoRunBehavior</span><span class="sxs-lookup"><span data-stu-id="21b33-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21b33-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21b33-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21b33-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="21b33-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="21b33-130">TurnOffAutoPlay</span><span class="sxs-lookup"><span data-stu-id="21b33-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="21b33-131">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="21b33-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="21b33-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="21b33-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="21b33-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21b33-133">Requirements</span></span>



| <span data-ttu-id="21b33-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21b33-134">Requirement</span></span> | <span data-ttu-id="21b33-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="21b33-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21b33-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b33-136">Minimum supported client</span></span><br/> | <span data-ttu-id="21b33-137">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="21b33-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="21b33-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b33-138">Minimum supported server</span></span><br/> | <span data-ttu-id="21b33-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="21b33-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="21b33-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="21b33-140">Namespace</span></span><br/>                | <span data-ttu-id="21b33-141">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="21b33-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="21b33-142">MOF</span><span class="sxs-lookup"><span data-stu-id="21b33-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="21b33-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="21b33-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="21b33-144">DLL</span><span class="sxs-lookup"><span data-stu-id="21b33-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="21b33-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21b33-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

