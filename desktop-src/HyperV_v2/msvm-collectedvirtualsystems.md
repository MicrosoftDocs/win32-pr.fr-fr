---
description: Msvm_CollectedVirtualSystems Class-associe le \_ VirtualSystemCollection MSVM aux objets MSVM \_ ComputerSystem contenus.
ms.assetid: ad783188-b60a-4271-aa2d-8050c36e70eb
title: Classe Msvm_CollectedVirtualSystems
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedVirtualSystems
- Msvm_CollectedVirtualSystems.Collection
- Msvm_CollectedVirtualSystems.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6775f41a6e2ae7e45bac642fcd32b8deaec3fda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119277"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="19a7f-103">MSVM \_ CollectedVirtualSystems, classe</span><span class="sxs-lookup"><span data-stu-id="19a7f-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="19a7f-104">Associe [**le \_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) aux objets [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenus.</span><span class="sxs-lookup"><span data-stu-id="19a7f-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="19a7f-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="19a7f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="19a7f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19a7f-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="19a7f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="19a7f-107">Members</span></span>

<span data-ttu-id="19a7f-108">La classe **MSVM \_ CollectedVirtualSystems** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="19a7f-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="19a7f-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19a7f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19a7f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="19a7f-110">Properties</span></span>

<span data-ttu-id="19a7f-111">La classe **MSVM \_ CollectedVirtualSystems** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="19a7f-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19a7f-112">**Collection**</span><span class="sxs-lookup"><span data-stu-id="19a7f-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19a7f-113">Type de données : **MSVM \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="19a7f-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="19a7f-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19a7f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19a7f-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="19a7f-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="19a7f-116">Un regroupement [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) ou un objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="19a7f-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="19a7f-117">**Membre**</span><span class="sxs-lookup"><span data-stu-id="19a7f-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19a7f-118">Type de données : **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="19a7f-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="19a7f-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="19a7f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19a7f-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="19a7f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="19a7f-121">Objet [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenant les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="19a7f-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19a7f-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19a7f-122">Requirements</span></span>



| <span data-ttu-id="19a7f-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19a7f-123">Requirement</span></span> | <span data-ttu-id="19a7f-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="19a7f-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19a7f-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19a7f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="19a7f-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19a7f-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="19a7f-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19a7f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="19a7f-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="19a7f-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="19a7f-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="19a7f-129">Namespace</span></span><br/>                | <span data-ttu-id="19a7f-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="19a7f-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="19a7f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="19a7f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19a7f-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19a7f-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="19a7f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="19a7f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19a7f-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="19a7f-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="19a7f-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19a7f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19a7f-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="19a7f-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

