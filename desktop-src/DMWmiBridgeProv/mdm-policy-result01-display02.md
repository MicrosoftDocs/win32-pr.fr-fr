---
title: Classe MDM_Policy_Result01_Display02
description: La \_ classe Display02 de la stratégie MDM \_ Result01 \_ représente les stratégies d’affichage.
ms.assetid: 9f8675d6-1fd7-4269-8059-9159622f03cb
keywords:
- Classe MDM_Policy_Result01_Display02
- Classe MDM_Policy_Result01_Display02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Display02
- MDM_Policy_Result01_Display02.InstanceID
- MDM_Policy_Result01_Display02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b8097d943e92343250802d63c4dfa2e5c77920
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465435"
---
# <a name="mdm_policy_result01_display02-class"></a><span data-ttu-id="c8c60-105">\_Classe Display02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="c8c60-105">MDM\_Policy\_Result01\_Display02 class</span></span>

<span data-ttu-id="c8c60-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="c8c60-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c8c60-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="c8c60-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c8c60-108">La \_ classe Display02 de la stratégie MDM \_ Result01 \_ représente les stratégies d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c8c60-108">The MDM\_Policy\_Result01\_Display02 class represents the display policies.</span></span>

<span data-ttu-id="c8c60-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="c8c60-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8c60-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8c60-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Display02
{
  string InstanceID;
  string ParentID;
  string TurnOffGdiDPIScalingForApps;
  string TurnOnGdiDPIScalingForApps;
};
```

## <a name="members"></a><span data-ttu-id="c8c60-111">Membres</span><span class="sxs-lookup"><span data-stu-id="c8c60-111">Members</span></span>

<span data-ttu-id="c8c60-112">La **classe \_ \_ Result01 \_ Display02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8c60-112">The **MDM\_Policy\_Result01\_Display02** class has these types of members:</span></span>

-   [<span data-ttu-id="c8c60-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8c60-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8c60-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c8c60-114">Properties</span></span>

<span data-ttu-id="c8c60-115">La **classe \_ \_ Result01 \_ Display02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c8c60-115">The **MDM\_Policy\_Result01\_Display02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c8c60-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c8c60-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8c60-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8c60-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8c60-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8c60-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8c60-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8c60-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8c60-120">**ID**</span><span class="sxs-lookup"><span data-stu-id="c8c60-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8c60-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8c60-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8c60-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c8c60-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8c60-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8c60-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8c60-124">TurnOffGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="c8c60-124">TurnOffGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnoffgdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8c60-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8c60-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8c60-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c8c60-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8c60-127">TurnOnGdiDPIScalingForApps</span><span class="sxs-lookup"><span data-stu-id="c8c60-127">TurnOnGdiDPIScalingForApps</span></span>](/windows/client-management/mdm/policy-csp-display#display-turnongdidpiscalingforapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8c60-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c8c60-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8c60-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="c8c60-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8c60-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8c60-130">Requirements</span></span>



| <span data-ttu-id="c8c60-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8c60-131">Requirement</span></span> | <span data-ttu-id="c8c60-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8c60-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8c60-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8c60-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c60-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8c60-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8c60-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8c60-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c60-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8c60-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c8c60-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8c60-137">Namespace</span></span><br/>                | <span data-ttu-id="c8c60-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="c8c60-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c8c60-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c8c60-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8c60-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8c60-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8c60-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c8c60-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8c60-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8c60-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

