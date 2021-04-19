---
description: Associe le \_ VirtualSystemCollection MSVM aux objets MSVM \_ ComputerSystem contenus.
ms.assetid: bbf7713a-b331-4b40-bcb4-3545c26c6f3a
title: Classe Msvm_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectedCollections
- Msvm_CollectedCollections.Collection
- Msvm_CollectedCollections.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16ec6ad77c44e0a4e9001a0cb77d227573635ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541242"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="99707-103">MSVM \_ CollectedCollections, classe</span><span class="sxs-lookup"><span data-stu-id="99707-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="99707-104">Associe [**le \_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) aux objets [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenus.</span><span class="sxs-lookup"><span data-stu-id="99707-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="99707-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="99707-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="99707-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99707-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="99707-107">Membres</span><span class="sxs-lookup"><span data-stu-id="99707-107">Members</span></span>

<span data-ttu-id="99707-108">La classe **MSVM \_ CollectedCollections** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="99707-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="99707-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="99707-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="99707-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="99707-110">Properties</span></span>

<span data-ttu-id="99707-111">La classe **MSVM \_ CollectedCollections** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="99707-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="99707-112">**Collection**</span><span class="sxs-lookup"><span data-stu-id="99707-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99707-113">Type de données : **MSVM \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="99707-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="99707-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="99707-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99707-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="99707-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="99707-116">Un regroupement [**MSVM \_ ManagementCollection**](msvm-managementcollection.md) ou un objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="99707-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="99707-117">**Membre**</span><span class="sxs-lookup"><span data-stu-id="99707-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="99707-118">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="99707-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="99707-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="99707-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="99707-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="99707-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="99707-121">Un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) contenant les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="99707-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99707-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99707-122">Requirements</span></span>



| <span data-ttu-id="99707-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99707-123">Requirement</span></span> | <span data-ttu-id="99707-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="99707-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99707-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99707-125">Minimum supported client</span></span><br/> | <span data-ttu-id="99707-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="99707-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="99707-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99707-127">Minimum supported server</span></span><br/> | <span data-ttu-id="99707-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="99707-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="99707-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="99707-129">Namespace</span></span><br/>                | <span data-ttu-id="99707-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="99707-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="99707-131">MOF</span><span class="sxs-lookup"><span data-stu-id="99707-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="99707-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="99707-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="99707-133">DLL</span><span class="sxs-lookup"><span data-stu-id="99707-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99707-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="99707-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="99707-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99707-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99707-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="99707-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

