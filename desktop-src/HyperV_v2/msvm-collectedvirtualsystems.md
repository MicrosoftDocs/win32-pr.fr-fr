---
description: Associe le \_ VirtualSystemCollection MSVM aux objets MSVM \_ ComputerSystem contenus.
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
ms.openlocfilehash: 0803eda14ffbaf21ee2bf4491bd835123b7191e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526238"
---
# <a name="msvm_collectedvirtualsystems-class"></a><span data-ttu-id="a33c5-103">MSVM \_ CollectedVirtualSystems, classe</span><span class="sxs-lookup"><span data-stu-id="a33c5-103">Msvm\_CollectedVirtualSystems class</span></span>

<span data-ttu-id="a33c5-104">Associe [**le \_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) aux objets [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenus.</span><span class="sxs-lookup"><span data-stu-id="a33c5-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="a33c5-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="a33c5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a33c5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a33c5-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedVirtualSystems : CIM_CollectedMSEs
{
  Msvm_VirtualSystemCollection REF Collection;
  Msvm_ComputerSystem          REF Member;
};
```

## <a name="members"></a><span data-ttu-id="a33c5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a33c5-107">Members</span></span>

<span data-ttu-id="a33c5-108">La classe **MSVM \_ CollectedVirtualSystems** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a33c5-108">The **Msvm\_CollectedVirtualSystems** class has these types of members:</span></span>

-   [<span data-ttu-id="a33c5-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a33c5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a33c5-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a33c5-110">Properties</span></span>

<span data-ttu-id="a33c5-111">La classe **MSVM \_ CollectedVirtualSystems** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a33c5-111">The **Msvm\_CollectedVirtualSystems** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a33c5-112">**Collection**</span><span class="sxs-lookup"><span data-stu-id="a33c5-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33c5-113">Type de données : **MSVM \_ VirtualSystemCollection**</span><span class="sxs-lookup"><span data-stu-id="a33c5-113">Data type: **Msvm\_VirtualSystemCollection**</span></span>
</dt> <dt>

<span data-ttu-id="a33c5-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a33c5-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a33c5-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="a33c5-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="a33c5-116">Un regroupement [**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md) ou un objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="a33c5-116">An [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="a33c5-117">**Membre**</span><span class="sxs-lookup"><span data-stu-id="a33c5-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a33c5-118">Type de données : **MSVM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="a33c5-118">Data type: **Msvm\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="a33c5-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="a33c5-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a33c5-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="a33c5-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="a33c5-121">Objet [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenant les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="a33c5-121">An [**Msvm\_ComputerSystem**](msvm-computersystem.md) object containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a33c5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a33c5-122">Requirements</span></span>



| <span data-ttu-id="a33c5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a33c5-123">Requirement</span></span> | <span data-ttu-id="a33c5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a33c5-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a33c5-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a33c5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a33c5-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a33c5-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a33c5-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a33c5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a33c5-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a33c5-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a33c5-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a33c5-129">Namespace</span></span><br/>                | <span data-ttu-id="a33c5-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="a33c5-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a33c5-131">MOF</span><span class="sxs-lookup"><span data-stu-id="a33c5-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a33c5-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a33c5-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a33c5-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a33c5-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a33c5-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a33c5-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a33c5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a33c5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33c5-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="a33c5-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

