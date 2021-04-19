---
description: Représente une association générique entre une collection d’éléments système managés et les membres de la collection.
ms.assetid: c9e2bbca-67be-41f2-a94c-cf4eaf5f4694
title: Classe CIM_CollectedMSEs (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedMSEs
- CIM_CollectedMSEs.Collection
- CIM_CollectedMSEs.Member
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bdf5c5d682f1b6e1b47b64100b3e00f5f79cebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524348"
---
# <a name="cim_collectedmses-class-hyper-v-management"></a><span data-ttu-id="e92b3-103">Classe CIM_CollectedMSEs (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="e92b3-103">CIM_CollectedMSEs class (Hyper-V management)</span></span>

<span data-ttu-id="e92b3-104">Représente une association générique entre une collection d’éléments système managés et les membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="e92b3-104">Represents a generic association between a collection of managed system elements and the members of the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e92b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e92b3-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::Collection"), AMENDMENT]
class CIM_CollectedMSEs : CIM_MemberOfCollection
{
  CIM_CollectionOfMSEs     REF Collection;
  CIM_ManagedSystemElement REF Member;
};
```

## <a name="members"></a><span data-ttu-id="e92b3-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e92b3-106">Members</span></span>

<span data-ttu-id="e92b3-107">La classe **CIM \_ CollectedMSEs** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e92b3-107">The **CIM\_CollectedMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="e92b3-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e92b3-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e92b3-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e92b3-109">Properties</span></span>

<span data-ttu-id="e92b3-110">La classe **CIM \_ CollectedMSEs** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="e92b3-110">The **CIM\_CollectedMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e92b3-111">**Collection**</span><span class="sxs-lookup"><span data-stu-id="e92b3-111">**Collection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b3-112">Type de données : **CIM \_ CollectionOfMSEs**</span><span class="sxs-lookup"><span data-stu-id="e92b3-112">Data type: **CIM\_CollectionOfMSEs**</span></span>
</dt> <dt>

<span data-ttu-id="e92b3-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e92b3-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e92b3-114">Qualificateurs : [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("collection")</span><span class="sxs-lookup"><span data-stu-id="e92b3-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Collection")</span></span>
</dt> </dl>

<span data-ttu-id="e92b3-115">Collection.</span><span class="sxs-lookup"><span data-stu-id="e92b3-115">The collection.</span></span>

</dd> <dt>

<span data-ttu-id="e92b3-116">**Membre**</span><span class="sxs-lookup"><span data-stu-id="e92b3-116">**Member**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e92b3-117">Type de données **: \_ CIM CIM**</span><span class="sxs-lookup"><span data-stu-id="e92b3-117">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="e92b3-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e92b3-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e92b3-119">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span><span class="sxs-lookup"><span data-stu-id="e92b3-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Member")</span></span>
</dt> </dl>

<span data-ttu-id="e92b3-120">Membres de la collection.</span><span class="sxs-lookup"><span data-stu-id="e92b3-120">The members of the collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e92b3-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e92b3-121">Requirements</span></span>



| <span data-ttu-id="e92b3-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e92b3-122">Requirement</span></span> | <span data-ttu-id="e92b3-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e92b3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e92b3-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e92b3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e92b3-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e92b3-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e92b3-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e92b3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e92b3-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e92b3-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e92b3-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e92b3-128">Namespace</span></span><br/>                | <span data-ttu-id="e92b3-129">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="e92b3-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e92b3-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e92b3-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e92b3-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e92b3-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e92b3-132">DLL</span><span class="sxs-lookup"><span data-stu-id="e92b3-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e92b3-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e92b3-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e92b3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e92b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e92b3-135">**\_MEMBEROFCOLLECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="e92b3-135">**CIM\_MemberOfCollection**</span></span>](cim-memberofcollection.md)
</dt> </dl>

 

