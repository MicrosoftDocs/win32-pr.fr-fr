---
title: Classe MDM_Policy_Config01_Storage02
description: La \_ classe Config01 Storage02 de la stratégie MDM \_ \_ configure les stratégies de stockage.
ms.assetid: 5c58e6d4-dfc6-4467-9a86-08eb31ccf28d
keywords:
- Classe MDM_Policy_Config01_Storage02
- Classe MDM_Policy_Config01_Storage02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Storage02
- MDM_Policy_Config01_Storage02.InstanceID
- MDM_Policy_Config01_Storage02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445c73158e032d888b5b1d0ec4496d2fd49c1ae1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103894"
---
# <a name="mdm_policy_config01_storage02-class"></a><span data-ttu-id="b5267-105">\_Classe Storage02 de la stratégie MDM \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="b5267-105">MDM\_Policy\_Config01\_Storage02 class</span></span>

<span data-ttu-id="b5267-106">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="b5267-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b5267-107">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="b5267-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b5267-108">La \_ classe Config01 Storage02 de la stratégie MDM \_ \_ configure les stratégies de stockage.</span><span class="sxs-lookup"><span data-stu-id="b5267-108">The MDM\_Policy\_Config01\_Storage02 class configures the storage policies.</span></span>

<span data-ttu-id="b5267-109">La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="b5267-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5267-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b5267-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Storage02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiskHealthModelUpdates;
  string EnhancedStorageDevices;
};
```

## <a name="members"></a><span data-ttu-id="b5267-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b5267-111">Members</span></span>

<span data-ttu-id="b5267-112">La **classe \_ \_ Config01 \_ Storage02 de la stratégie MDM** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b5267-112">The **MDM\_Policy\_Config01\_Storage02** class has these types of members:</span></span>

-   [<span data-ttu-id="b5267-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5267-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5267-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b5267-114">Properties</span></span>

<span data-ttu-id="b5267-115">La **classe \_ \_ Config01 \_ Storage02 de la stratégie MDM** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b5267-115">The **MDM\_Policy\_Config01\_Storage02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b5267-116">AllowDiskHealthModelUpdates</span><span class="sxs-lookup"><span data-stu-id="b5267-116">AllowDiskHealthModelUpdates</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-allowdiskhealthmodelupdates)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5267-117">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="b5267-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b5267-118">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5267-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b5267-119">EnhancedStorageDevices</span><span class="sxs-lookup"><span data-stu-id="b5267-119">EnhancedStorageDevices</span></span>](/windows/client-management/mdm/policy-csp-storage#storage-enhancedstoragedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5267-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5267-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5267-121">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b5267-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5267-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b5267-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5267-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5267-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5267-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5267-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5267-125">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5267-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b5267-126">**ID**</span><span class="sxs-lookup"><span data-stu-id="b5267-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5267-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="b5267-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b5267-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b5267-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5267-129">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b5267-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b5267-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5267-130">Requirements</span></span>



| <span data-ttu-id="b5267-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5267-131">Requirement</span></span> | <span data-ttu-id="b5267-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5267-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5267-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5267-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b5267-134">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5267-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5267-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5267-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b5267-136">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5267-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b5267-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b5267-137">Namespace</span></span><br/>                | <span data-ttu-id="b5267-138">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="b5267-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b5267-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b5267-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5267-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5267-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5267-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b5267-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5267-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5267-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

