---
title: Classe MDM_Policy_Result01_Storage02
description: La \_ classe Result01 Storage02 de la stratégie MDM \_ \_ représente les stratégies de stockage disponibles.
ms.assetid: e0e3b867-38b5-4b10-a13e-6f99b8ff6db3
keywords:
- Classe MDM_Policy_Result01_Storage02
- Classe MDM_Policy_Result01_Storage02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Storage02
- MDM_Policy_Result01_Storage02.InstanceID
- MDM_Policy_Result01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63381b34c88ebc590577eec9a11f603ea5325649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032739"
---
# <a name="mdm_policy_result01_storage02-class"></a><span data-ttu-id="37172-105">\_Classe Storage02 de la stratégie MDM \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="37172-105">MDM\_Policy\_Result01\_Storage02 class</span></span>

<span data-ttu-id="37172-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="37172-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="37172-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="37172-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="37172-108">La \_ classe Result01 Storage02 de la stratégie MDM \_ \_ représente les stratégies de stockage disponibles.</span><span class="sxs-lookup"><span data-stu-id="37172-108">The MDM\_Policy\_Result01\_Storage02 class represents the available storage policies.</span></span>

<span data-ttu-id="37172-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="37172-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="37172-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37172-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="37172-111">Membres</span><span class="sxs-lookup"><span data-stu-id="37172-111">Members</span></span>

<span data-ttu-id="37172-112">La **classe \_ \_ Result01 \_ Storage02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="37172-112">The **MDM\_Policy\_Result01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="37172-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37172-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="37172-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37172-114">Properties</span></span>

<span data-ttu-id="37172-115">La **classe \_ \_ Result01 \_ Storage02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="37172-115">The **MDM\_Policy\_Result01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="37172-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="37172-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37172-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="37172-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="37172-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="37172-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="37172-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="37172-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="37172-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37172-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37172-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="37172-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37172-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="37172-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37172-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37172-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37172-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37172-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37172-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37172-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="37172-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="37172-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="37172-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="37172-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="37172-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="37172-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="37172-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="37172-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37172-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37172-130">Requirements</span></span>



| <span data-ttu-id="37172-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37172-131">Requirement</span></span> | <span data-ttu-id="37172-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="37172-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37172-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37172-133">Minimum supported client</span></span><br/> | <span data-ttu-id="37172-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37172-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="37172-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37172-135">Minimum supported server</span></span><br/> | <span data-ttu-id="37172-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37172-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="37172-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37172-137">Namespace</span></span><br/>                | <span data-ttu-id="37172-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="37172-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="37172-139">MOF</span><span class="sxs-lookup"><span data-stu-id="37172-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37172-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37172-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="37172-141">DLL</span><span class="sxs-lookup"><span data-stu-id="37172-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37172-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37172-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

