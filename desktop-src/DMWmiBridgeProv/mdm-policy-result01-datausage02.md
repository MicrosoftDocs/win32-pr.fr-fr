---
title: Classe MDM_Policy_Result01_DataUsage02
description: La \_ classe Result01 DataUsage02 de la stratégie MDM \_ \_ représente les stratégies d’utilisation des données disponibles.
ms.assetid: 4efcab61-2060-44dc-bc3c-7b23802fa284
keywords:
- Classe MDM_Policy_Result01_DataUsage02
- Classe MDM_Policy_Result01_DataUsage02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DataUsage02
- MDM_Policy_Result01_DataUsage02.InstanceID
- MDM_Policy_Result01_DataUsage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d97bcfba122bd3d974025975a69ba6a5be9c8ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466199"
---
# <a name="mdm_policy_result01_datausage02-class"></a><span data-ttu-id="46460-105">\_Classe DataUsage02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="46460-105">MDM\_Policy\_Result01\_DataUsage02 class</span></span>

<span data-ttu-id="46460-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="46460-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="46460-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="46460-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="46460-108">La \_ classe Result01 DataUsage02 de la stratégie MDM \_ \_ représente les stratégies d’utilisation des données disponibles.</span><span class="sxs-lookup"><span data-stu-id="46460-108">The MDM\_Policy\_Result01\_DataUsage02 class represents the available data usage policies.</span></span>

<span data-ttu-id="46460-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="46460-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46460-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46460-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DataUsage02
{
  string InstanceID;
  string ParentID;
  string SetCost3G;
  string SetCost4G;
};
```

## <a name="members"></a><span data-ttu-id="46460-111">Membres</span><span class="sxs-lookup"><span data-stu-id="46460-111">Members</span></span>

<span data-ttu-id="46460-112">La **classe \_ \_ Result01 \_ DataUsage02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="46460-112">The **MDM\_Policy\_Result01\_DataUsage02** class has these types of members:</span></span>

-   [<span data-ttu-id="46460-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46460-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46460-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="46460-114">Properties</span></span>

<span data-ttu-id="46460-115">La **classe \_ \_ Result01 \_ DataUsage02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="46460-115">The **MDM\_Policy\_Result01\_DataUsage02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46460-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46460-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46460-117">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46460-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46460-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46460-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46460-119">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46460-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="46460-120">**ID**</span><span class="sxs-lookup"><span data-stu-id="46460-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46460-121">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46460-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46460-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="46460-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46460-123">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="46460-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46460-124">SetCost3G</span><span class="sxs-lookup"><span data-stu-id="46460-124">SetCost3G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost3g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46460-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46460-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46460-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46460-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="46460-127">SetCost4G</span><span class="sxs-lookup"><span data-stu-id="46460-127">SetCost4G</span></span>](/windows/client-management/mdm/policy-csp-datausage#datausage-setcost4g)
</dt> <dd> <dl> <dt>

<span data-ttu-id="46460-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="46460-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46460-129">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="46460-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46460-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46460-130">Requirements</span></span>



| <span data-ttu-id="46460-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46460-131">Requirement</span></span> | <span data-ttu-id="46460-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="46460-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46460-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46460-133">Minimum supported client</span></span><br/> | <span data-ttu-id="46460-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46460-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46460-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46460-135">Minimum supported server</span></span><br/> | <span data-ttu-id="46460-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="46460-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="46460-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="46460-137">Namespace</span></span><br/>                | <span data-ttu-id="46460-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="46460-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="46460-139">MOF</span><span class="sxs-lookup"><span data-stu-id="46460-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46460-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46460-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="46460-141">DLL</span><span class="sxs-lookup"><span data-stu-id="46460-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46460-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46460-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

