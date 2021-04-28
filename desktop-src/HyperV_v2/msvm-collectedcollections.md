---
description: Msvm_CollectedCollections Class-associe le \_ VirtualSystemCollection MSVM aux objets MSVM \_ ComputerSystem contenus.
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
ms.openlocfilehash: 83719d364fac22923d68206c8cfe7d37adad5edb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112127"
---
# <a name="msvm_collectedcollections-class"></a><span data-ttu-id="f07b7-103">MSVM \_ CollectedCollections, classe</span><span class="sxs-lookup"><span data-stu-id="f07b7-103">Msvm\_CollectedCollections class</span></span>

<span data-ttu-id="f07b7-104">Associe [**le \_ VirtualSystemCollection MSVM**](msvm-virtualsystemcollection.md) aux objets [**MSVM \_ ComputerSystem**](msvm-computersystem.md) contenus.</span><span class="sxs-lookup"><span data-stu-id="f07b7-104">Associates the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to the contained [**Msvm\_ComputerSystem**](msvm-computersystem.md) objects.</span></span>

<span data-ttu-id="f07b7-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="f07b7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f07b7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f07b7-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectedCollections : CIM_CollectedMSEs
{
  Msvm_ManagementCollection REF Collection;
  CIM_CollectionOfMSEs      REF Member;
};
```

## <a name="members"></a><span data-ttu-id="f07b7-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f07b7-107">Members</span></span>

<span data-ttu-id="f07b7-108">La classe **MSVM \_ CollectedCollections** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f07b7-108">The **Msvm\_CollectedCollections** class has these types of members:</span></span>

-   [<span data-ttu-id="f07b7-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f07b7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f07b7-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f07b7-110">Properties</span></span>

<span data-ttu-id="f07b7-111">La classe **MSVM \_ CollectedCollections** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f07b7-111">The **Msvm\_CollectedCollections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f07b7-112">**Collection**</span><span class="sxs-lookup"><span data-stu-id="f07b7-112">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f07b7-113">Type de données : **MSVM \_ ManagementCollection**</span><span class="sxs-lookup"><span data-stu-id="f07b7-113">Data type: **Msvm\_ManagementCollection**</span></span>
</dt> <dt>

<span data-ttu-id="f07b7-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f07b7-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f07b7-115">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="f07b7-115">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="f07b7-116">Un regroupement [**MSVM \_ ManagementCollection**](msvm-managementcollection.md) ou un objet « Bag » qui représente la collection.</span><span class="sxs-lookup"><span data-stu-id="f07b7-116">An [**Msvm\_ManagementCollection**](msvm-managementcollection.md) grouping or 'bag' object that represents the collection.</span></span>

</dd> <dt>

<span data-ttu-id="f07b7-117">**Membre**</span><span class="sxs-lookup"><span data-stu-id="f07b7-117">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f07b7-118">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="f07b7-118">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="f07b7-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f07b7-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f07b7-120">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="f07b7-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="f07b7-121">Un [**\_ CollectionOfMSEs CIM**](cim-collectionofmses.md) contenant les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="f07b7-121">A [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) containing the members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f07b7-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f07b7-122">Requirements</span></span>



| <span data-ttu-id="f07b7-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f07b7-123">Requirement</span></span> | <span data-ttu-id="f07b7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f07b7-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f07b7-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f07b7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f07b7-126">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f07b7-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f07b7-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f07b7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f07b7-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f07b7-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f07b7-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f07b7-129">Namespace</span></span><br/>                | <span data-ttu-id="f07b7-130">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="f07b7-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f07b7-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f07b7-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f07b7-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f07b7-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f07b7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f07b7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f07b7-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f07b7-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f07b7-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f07b7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f07b7-136">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="f07b7-136">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> </dl>

 

